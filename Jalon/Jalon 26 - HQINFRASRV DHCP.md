# dhcpd.conf
***
***Voici le fichier de configuration du DHCP sur HQINFRASRV***
```
HQINFRADHCP sans failover /etc/dhcp/dhcpd.conf
default-lease-time 7200;
max-lease-time 7200;


ddns-update-style none;

failover peer "dhcp-failover" {
    primary;
    address 10.5.10.2;
    peer address 10.5.10.3;
    port 647;
    max-response-delay 60;
    max-unacked-updates 10;
    mclt 300;
    split 128;
    load balance max seconds 3;
}

subnet 10.5.20.0 netmask 255.255.254.0 {
    option routers 10.5.21.254;
    option domain-name-servers 10.5.10.1;
    option domain-name "wsl2024.org";
    pool {
        failover peer "dhcp-failover";
        range 10.5.20.100 10.5.21.200;
    }
}
[12:11]
HQINFRASRV dhcp avec failover default-lease-time 7200;
max-lease-time 7200;

option ntp-servers hqinfrasrv.wsl2024.org;

ddns-update-style none;

failover peer "dhcp-failover" {
    primary;
    address 10.5.20.1;
    peer address 10.5.10.1;
    port 647;
    max-response-delay 60;
    max-unacked-updates 10;
    mclt 300;
    split 128;
    load balance max seconds 3;
}

subnet 10.5.20.0 netmask 255.255.254.0 {
    range 10.5.20.100 10.5.21.200;
    option routers 10.5.21.254;
    option domain-name-servers 10.5.10.1;
    option domain-name "wsl2024.org";
    option ntp-servers hqinfrasrv.wsl2024.org;
    peer "dhcp-failover";
}
```
