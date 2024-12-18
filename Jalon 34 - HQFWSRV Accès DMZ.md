# Règle de HQFWSRV pour un accès à DMZ
```
<nat>
	<outbound>
		<mode>automatic</mode>
	</outbound>
	<separator></separator>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>80</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>80</local-port>
		<interface>opt1</interface>
		<descr><![CDATA[http]]></descr>
		<associated-rule-id>nat_675e6175ee5408.95522659</associated-rule-id>
		<created>
			<time>1734238581</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734257811</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>80</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>80</local-port>
		<interface>openvpn</interface>
		<descr><![CDATA[http]]></descr>
		<associated-rule-id>nat_675ead3c6dabe0.21211094</associated-rule-id>
		<updated>
			<time>1734257980</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734257980</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>80</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>80</local-port>
		<interface>wan</interface>
		<descr><![CDATA[http]]></descr>
		<associated-rule-id>nat_675eac9be75ed3.42747058</associated-rule-id>
		<created>
			<time>1734257819</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734257841</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>80</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>80</local-port>
		<interface>lan</interface>
		<descr><![CDATA[http]]></descr>
		<associated-rule-id>nat_675eacb7d23479.07436582</associated-rule-id>
		<updated>
			<time>1734257847</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734257847</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>443</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>443</local-port>
		<interface>opt1</interface>
		<descr><![CDATA[https]]></descr>
		<associated-rule-id>nat_675e61fa076599.79606385</associated-rule-id>
		<created>
			<time>1734238714</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734257703</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>443</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>443</local-port>
		<interface>lan</interface>
		<descr><![CDATA[https]]></descr>
		<associated-rule-id>nat_675eacc1704908.64579070</associated-rule-id>
		<updated>
			<time>1734257857</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734257857</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>443</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>443</local-port>
		<interface>openvpn</interface>
		<descr><![CDATA[https]]></descr>
		<associated-rule-id>nat_675ead4cf3d7c0.20219459</associated-rule-id>
		<updated>
			<time>1734257996</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734257996</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>443</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>443</local-port>
		<interface>wan</interface>
		<descr><![CDATA[https]]></descr>
		<associated-rule-id>nat_675eacca5048d7.96435614</associated-rule-id>
		<updated>
			<time>1734257866</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734257866</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>3389</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>3389</local-port>
		<interface>opt1</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_675e6185679424.80089889</associated-rule-id>
		<created>
			<time>1734238597</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734257793</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>3389</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>3389</local-port>
		<interface>lan</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_675eacf458e117.39845255</associated-rule-id>
		<updated>
			<time>1734257908</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734257908</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>3389</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>3389</local-port>
		<interface>wan</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_675eacff44f201.05925534</associated-rule-id>
		<updated>
			<time>1734257919</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734257919</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>3389</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>3389</local-port>
		<interface>openvpn</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_675ead56baad64.65372907</associated-rule-id>
		<updated>
			<time>1734258006</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734258006</time>
			<username><![CDATA[admin@10.5.10.8 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>135</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>135</local-port>
		<interface>openvpn</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_6760e37ba4d444.85553510</associated-rule-id>
		<created>
			<time>1734402939</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734403041</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>135</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>135</local-port>
		<interface>wan</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_6760e3fc4d6282.54186851</associated-rule-id>
		<updated>
			<time>1734403068</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403068</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>135</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>135</local-port>
		<interface>lan</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_6760e40e955f27.50399532</associated-rule-id>
		<updated>
			<time>1734403086</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403086</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>135</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>135</local-port>
		<interface>opt1</interface>
		<descr><![CDATA[ms rdp]]></descr>
		<associated-rule-id>nat_6760e41a87c568.01596738</associated-rule-id>
		<updated>
			<time>1734403098</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403098</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>445</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>445</local-port>
		<interface>wan</interface>
		<descr><![CDATA[ms ds]]></descr>
		<associated-rule-id>nat_675e62325ed802.70743995</associated-rule-id>
		<updated>
			<time>1734238770</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734238770</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>445</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>445</local-port>
		<interface>opt1</interface>
		<descr><![CDATA[ms ds]]></descr>
		<associated-rule-id>nat_6760e437eb2890.22326073</associated-rule-id>
		<updated>
			<time>1734403127</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403127</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>445</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>445</local-port>
		<interface>lan</interface>
		<descr><![CDATA[ms ds]]></descr>
		<associated-rule-id>nat_6760e427dee172.96044022</associated-rule-id>
		<updated>
			<time>1734403111</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403111</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>445</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>445</local-port>
		<interface>openvpn</interface>
		<descr><![CDATA[ms ds]]></descr>
		<associated-rule-id>nat_6760e442ab67a2.53573327</associated-rule-id>
		<updated>
			<time>1734403138</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403138</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>1512</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>1512</local-port>
		<interface>wan</interface>
		<descr><![CDATA[ms wins]]></descr>
		<associated-rule-id>nat_675e624c1a0766.93778993</associated-rule-id>
		<updated>
			<time>1734238796</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734238796</time>
			<username><![CDATA[admin@10.5.10.2 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>1512</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>1512</local-port>
		<interface>lan</interface>
		<descr><![CDATA[ms wins]]></descr>
		<associated-rule-id>nat_6760e45017b4b7.26419226</associated-rule-id>
		<updated>
			<time>1734403152</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403152</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>1512</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>1512</local-port>
		<interface>opt1</interface>
		<descr><![CDATA[ms wins]]></descr>
		<associated-rule-id>nat_6760e459b462d4.10325994</associated-rule-id>
		<updated>
			<time>1734403161</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403161</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>53</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>53</local-port>
		<interface>opt1</interface>
		<descr><![CDATA[ms wins]]></descr>
		<associated-rule-id>nat_6760e553f104a3.60056127</associated-rule-id>
		<updated>
			<time>1734403411</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403411</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>1512</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>1512</local-port>
		<interface>wan</interface>
		<descr><![CDATA[ms wins]]></descr>
		<associated-rule-id>nat_6760e46267d9a0.83221669</associated-rule-id>
		<created>
			<time>1734403170</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
		<updated>
			<time>1734403426</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
	</rule>
	<rule>
		<source>
			<any></any>
		</source>
		<destination>
			<network>wan</network>
			<port>88</port>
		</destination>
		<ipprotocol>inet</ipprotocol>
		<protocol>tcp/udp</protocol>
		<target>10.5.30.1</target>
		<local-port>88</local-port>
		<interface>wan</interface>
		<descr><![CDATA[ms wins]]></descr>
		<associated-rule-id>nat_6760e57c74b830.81172416</associated-rule-id>
		<updated>
			<time>1734403452</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</updated>
		<created>
			<time>1734403452</time>
			<username><![CDATA[admin@10.5.30.1 (Local Database)]]></username>
		</created>
	</rule>
</nat>
```
