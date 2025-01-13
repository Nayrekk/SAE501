# Règle de filtrage actif sur HQFWSRV
```

<filter>
	<rule>
		<id></id>
		<tracker>1734239369</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>4443</port>
		</destination>
		<descr><![CDATA[VPN]]></descr>
		<created>
			<time>1734239369</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734386350</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<id></id>
		<tracker>1734239656</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.10.3</address>
			<port>465</port>
		</destination>
		<descr><![CDATA[Mail]]></descr>
		<created>
			<time>1734239656</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734239795</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<id></id>
		<tracker>1734239777</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.10.3</address>
			<port>993</port>
		</destination>
		<descr><![CDATA[mail]]></descr>
		<updated>
			<time>1734239777</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734239777</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>445</port>
		</destination>
		<descr><![CDATA[NAT ms ds]]></descr>
		<associated-rule-id>nat_675e62325ed802.70743995</associated-rule-id>
		<tracker>1734238770</tracker>
		<created>
			<time>1734238770</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>1512</port>
		</destination>
		<descr><![CDATA[NAT ms wins]]></descr>
		<associated-rule-id>nat_675e624c1a0766.93778993</associated-rule-id>
		<tracker>1734238796</tracker>
		<created>
			<time>1734238796</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>80</port>
		</destination>
		<descr><![CDATA[NAT http]]></descr>
		<associated-rule-id>nat_675eac9be75ed3.42747058</associated-rule-id>
		<tracker>1734257819</tracker>
		<created>
			<time>1734257819</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>443</port>
		</destination>
		<descr><![CDATA[NAT https]]></descr>
		<associated-rule-id>nat_675eacca5048d7.96435614</associated-rule-id>
		<tracker>1734257866</tracker>
		<created>
			<time>1734257866</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734350407</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>217.5.160.1</address>
			<port>443</port>
		</destination>
		<descr><![CDATA[NAT https]]></descr>
		<updated>
			<time>1734350407</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734350407</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>3389</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_675eacff44f201.05925534</associated-rule-id>
		<tracker>1734257919</tracker>
		<created>
			<time>1734257919</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734343118</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>135</port>
		</destination>
		<descr><![CDATA[RPC ENDpoint Mapper]]></descr>
		<updated>
			<time>1734343118</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734343118</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734342830</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>3391</port>
		</destination>
		<descr><![CDATA[Remote Desktop Gateway (RD gateway) avec NAT Transversal (RPC over HTTPS))]]></descr>
		<updated>
			<time>1734342830</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734342830</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734343078</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>49152-65535</port>
		</destination>
		<descr><![CDATA[Ports dynamiques RPC]]></descr>
		<updated>
			<time>1734343078</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734343078</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734343193</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>137-139</port>
		</destination>
		<descr><![CDATA[Pour fonctionnalit&eacute;s li&eacute;es au partage de fichiers et d&#039;imprimantes]]></descr>
		<created>
			<time>1734343193</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734343385</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<id></id>
		<tracker>1734343484</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>2179</port>
		</destination>
		<descr><![CDATA[Hyper-V via VmConnect]]></descr>
		<updated>
			<time>1734343484</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734343484</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734345080</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>389</port>
		</destination>
		<descr><![CDATA[LDAP]]></descr>
		<created>
			<time>1734345080</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734345100</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<id></id>
		<tracker>1734345130</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>636</port>
		</destination>
		<descr><![CDATA[LDAPs via SSL/TLS]]></descr>
		<updated>
			<time>1734345130</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734345130</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734345159</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>3268</port>
		</destination>
		<descr><![CDATA[Global Catalog (GC)]]></descr>
		<created>
			<time>1734345159</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734345192</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<id></id>
		<tracker>1734345238</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>3269</port>
		</destination>
		<descr><![CDATA[Global Catalog via SSL/TLS]]></descr>
		<updated>
			<time>1734345238</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734345238</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734345356</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>88</port>
		</destination>
		<descr><![CDATA[Kerberos]]></descr>
		<created>
			<time>1734345356</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734345508</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<id></id>
		<tracker>1734345530</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>53</port>
		</destination>
		<descr><![CDATA[DNS]]></descr>
		<updated>
			<time>1734345530</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734345530</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734354738</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>67-68</port>
		</destination>
		<descr><![CDATA[DHCP]]></descr>
		<updated>
			<time>1734354738</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734354738</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734354773</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>514</port>
		</destination>
		<descr><![CDATA[Syslog]]></descr>
		<updated>
			<time>1734354773</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734354773</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734354837</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>5985-5986</port>
		</destination>
		<descr><![CDATA[PowerShell Remoting via WinRM (http https)]]></descr>
		<updated>
			<time>1734354837</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734354837</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734366604</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>1812-1813</port>
		</destination>
		<descr><![CDATA[Ath Radius / Gestion compte Radius]]></descr>
		<updated>
			<time>1734366604</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734366604</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734366624</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<address>10.5.30.1</address>
			<port>123</port>
		</destination>
		<descr><![CDATA[NTP]]></descr>
		<updated>
			<time>1734366624</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734366624</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734349519</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<any></any>
			<port>22</port>
		</destination>
		<descr></descr>
		<updated>
			<time>1734349519</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734349519</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734349564</tracker>
		<type>pass</type>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>icmp</protocol>
		<icmptype>echorep,echoreq</icmptype>
		<source>
			<any></any>
		</source>
		<destination>
			<any></any>
		</destination>
		<descr></descr>
		<updated>
			<time>1734349564</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734349564</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>135</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_6760e3fc4d6282.54186851</associated-rule-id>
		<tracker>1734403068</tracker>
		<created>
			<time>1734403068</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>1512</port>
		</destination>
		<descr><![CDATA[NAT ms wins]]></descr>
		<associated-rule-id>nat_6760e46267d9a0.83221669</associated-rule-id>
		<tracker>1734403170</tracker>
		<created>
			<time>1734403170</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>wan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>88</port>
		</destination>
		<descr><![CDATA[NAT ms wins]]></descr>
		<associated-rule-id>nat_6760e57c74b830.81172416</associated-rule-id>
		<tracker>1734403452</tracker>
		<created>
			<time>1734403452</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<type>pass</type>
		<ipprotocol>inet</ipprotocol>
		<descr><![CDATA[Default allow LAN to any rule]]></descr>
		<interface>lan</interface>
		<tracker>0100000101</tracker>
		<source>
			<network>lan</network>
		</source>
		<destination>
			<any></any>
		</destination>
	</rule>
	<rule>
		<type>pass</type>
		<ipprotocol>inet6</ipprotocol>
		<descr><![CDATA[Default allow LAN IPv6 to any rule]]></descr>
		<interface>lan</interface>
		<tracker>0100000102</tracker>
		<source>
			<network>lan</network>
		</source>
		<destination>
			<any></any>
		</destination>
	</rule>
	<rule>
		<id></id>
		<tracker>1734246070</tracker>
		<type>pass</type>
		<interface>lan</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<source>
			<any></any>
		</source>
		<destination>
			<any></any>
		</destination>
		<descr></descr>
		<updated>
			<time>1734246070</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734246070</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>lan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>80</port>
		</destination>
		<descr><![CDATA[NAT http]]></descr>
		<associated-rule-id>nat_675eacb7d23479.07436582</associated-rule-id>
		<tracker>1734257847</tracker>
		<created>
			<time>1734257847</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>lan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>443</port>
		</destination>
		<descr><![CDATA[NAT https]]></descr>
		<associated-rule-id>nat_675eacc1704908.64579070</associated-rule-id>
		<tracker>1734257857</tracker>
		<created>
			<time>1734257857</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>lan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>3389</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_675eacf458e117.39845255</associated-rule-id>
		<tracker>1734257908</tracker>
		<created>
			<time>1734257908</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>lan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>135</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_6760e40e955f27.50399532</associated-rule-id>
		<tracker>1734403086</tracker>
		<created>
			<time>1734403086</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>lan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>445</port>
		</destination>
		<descr><![CDATA[NAT ms ds]]></descr>
		<associated-rule-id>nat_6760e427dee172.96044022</associated-rule-id>
		<tracker>1734403111</tracker>
		<created>
			<time>1734403111</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>lan</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>1512</port>
		</destination>
		<descr><![CDATA[NAT ms wins]]></descr>
		<associated-rule-id>nat_6760e45017b4b7.26419226</associated-rule-id>
		<tracker>1734403152</tracker>
		<created>
			<time>1734403152</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734239393</tracker>
		<type>pass</type>
		<interface>openvpn</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<source>
			<any></any>
		</source>
		<destination>
			<any></any>
		</destination>
		<descr></descr>
		<updated>
			<time>1734239393</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734239393</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>openvpn</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>80</port>
		</destination>
		<descr><![CDATA[NAT http]]></descr>
		<associated-rule-id>nat_675ead3c6dabe0.21211094</associated-rule-id>
		<tracker>1734257980</tracker>
		<created>
			<time>1734257980</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>openvpn</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>443</port>
		</destination>
		<descr><![CDATA[NAT https]]></descr>
		<associated-rule-id>nat_675ead4cf3d7c0.20219459</associated-rule-id>
		<tracker>1734257996</tracker>
		<created>
			<time>1734257996</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>openvpn</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>3389</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_675ead56baad64.65372907</associated-rule-id>
		<tracker>1734258006</tracker>
		<created>
			<time>1734258006</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>openvpn</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>135</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_6760e37ba4d444.85553510</associated-rule-id>
		<tracker>1734402939</tracker>
		<created>
			<time>1734402939</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>openvpn</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>445</port>
		</destination>
		<descr><![CDATA[NAT ms ds]]></descr>
		<associated-rule-id>nat_6760e442ab67a2.53573327</associated-rule-id>
		<tracker>1734403138</tracker>
		<created>
			<time>1734403138</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734234022</tracker>
		<type>pass</type>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<source>
			<any></any>
		</source>
		<destination>
			<any></any>
		</destination>
		<descr></descr>
		<updated>
			<time>1734234022</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734234022</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>80</port>
		</destination>
		<descr><![CDATA[NAT http]]></descr>
		<associated-rule-id>nat_675e6175ee5408.95522659</associated-rule-id>
		<tracker>1734238581</tracker>
		<created>
			<time>1734238581</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>3389</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_675e6185679424.80089889</associated-rule-id>
		<tracker>1734238597</tracker>
		<created>
			<time>1734238597</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>443</port>
		</destination>
		<descr><![CDATA[NAT https]]></descr>
		<associated-rule-id>nat_675e61fa076599.79606385</associated-rule-id>
		<tracker>1734238714</tracker>
		<created>
			<time>1734238714</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>135</port>
		</destination>
		<descr><![CDATA[NAT ms rdp]]></descr>
		<associated-rule-id>nat_6760e41a87c568.01596738</associated-rule-id>
		<tracker>1734403098</tracker>
		<created>
			<time>1734403098</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>445</port>
		</destination>
		<descr><![CDATA[NAT ms ds]]></descr>
		<associated-rule-id>nat_6760e437eb2890.22326073</associated-rule-id>
		<tracker>1734403127</tracker>
		<created>
			<time>1734403127</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>1512</port>
		</destination>
		<descr><![CDATA[NAT ms wins]]></descr>
		<associated-rule-id>nat_6760e459b462d4.10325994</associated-rule-id>
		<tracker>1734403161</tracker>
		<created>
			<time>1734403161</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<interface>opt1</interface>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<destination>
			<address>10.5.30.1</address>
			<port>53</port>
		</destination>
		<descr><![CDATA[NAT ms wins]]></descr>
		<associated-rule-id>nat_6760e553f104a3.60056127</associated-rule-id>
		<tracker>1734403411</tracker>
		<created>
			<time>1734403411</time>
			<username><![CDATA[NAT Port Forward]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734332035</tracker>
		<type>pass</type>
		<interface>opt2</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<protocol>tcp/udp</protocol>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wanip</network>
			<port>4443</port>
		</destination>
		<descr><![CDATA[VPN]]></descr>
		<updated>
			<time>1734239369</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734239369</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<id></id>
		<tracker>1734236201</tracker>
		<type>pass</type>
		<interface>opt2</interface>
		<ipprotocol>inet</ipprotocol>
		<tag></tag>
		<tagged></tagged>
		<max></max>
		<max-src-nodes></max-src-nodes>
		<max-src-conn></max-src-conn>
		<max-src-states></max-src-states>
		<statetimeout></statetimeout>
		<statetype><![CDATA[keep state]]></statetype>
		<os></os>
		<source>
			<any></any>
		</source>
		<destination>
			<any></any>
		</destination>
		<descr></descr>
		<updated>
			<time>1734236201</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734236201</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<separator>
		<opt1></opt1>
		<opt2></opt2>
		<wan></wan>
		<openvpn></openvpn>
	</separator>
</filter>
```
