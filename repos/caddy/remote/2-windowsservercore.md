## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:c201558abd66b8c0fc4de32845be7c37c830fb7d7d0dcc398a6f8330fe0985b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull caddy@sha256:48029b2af873b654ef528a0468771152757f3aff498460a8233b00f3107c5e01
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416891890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce597dcf172032536d384eeef84fcbd6ca6c24933f291d866281f8975c6df6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 22:50:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 04 Jan 2021 18:17:16 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:17:46 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 04 Jan 2021 18:17:48 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 04 Jan 2021 18:17:49 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 04 Jan 2021 18:17:50 GMT
VOLUME [c:/config]
# Mon, 04 Jan 2021 18:17:50 GMT
VOLUME [c:/data]
# Mon, 04 Jan 2021 18:17:51 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:17:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:17:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:17:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:17:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:17:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:17:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:17:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:17:56 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:17:57 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:17:58 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:18:13 GMT
RUN caddy version
# Mon, 04 Jan 2021 18:18:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433ced4e59cd32da7d04608be235ec50650c9160c8742a10c9a60ae7294d7f52`  
		Last Modified: Wed, 09 Dec 2020 22:59:41 GMT  
		Size: 9.2 MB (9243267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1759fc5bf9fd13de97d6dca0f9e54baca002ebb4de30d04d4f84a7211df1744d`  
		Last Modified: Mon, 04 Jan 2021 18:54:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285c940b532630e8eab2efe3c31972514bb49b5e2b89957b4d50bf3e363ad40`  
		Last Modified: Mon, 04 Jan 2021 18:54:16 GMT  
		Size: 16.5 MB (16453020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f12516491e9de826b83073758da335a09abc886022d25d41c15bb694b25b2b5`  
		Last Modified: Mon, 04 Jan 2021 18:54:11 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b444ea4e9fd60f4a30fadd6823d4ede385fee2773c231bcb782642f0c108273b`  
		Last Modified: Mon, 04 Jan 2021 18:54:16 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecdc2ce806c311d8120e18e152f9f5fe11ca412b8e7a7690c384967c35f8e8a`  
		Last Modified: Mon, 04 Jan 2021 18:54:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3bc1e403611a29a16b08bf8b34797e8014fed9c9ba191ae7b663e84afa2052`  
		Last Modified: Mon, 04 Jan 2021 18:54:09 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b648c950e7f7ea87f2aab5da8e6e709dacaeeb617674b8c87ed74cb45fbfeae9`  
		Last Modified: Mon, 04 Jan 2021 18:54:08 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae90ccca399f11e47236a597dc0ba255b03dfd9e3dea78cbf63355306de9725`  
		Last Modified: Mon, 04 Jan 2021 18:54:07 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eceb6ca597121b71b7a353ab4ba5a9487799ee72acaa166e594646004db6dcce`  
		Last Modified: Mon, 04 Jan 2021 18:54:06 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c725bbf9ff1e2ac20ae14e252b08c1cc99bc24386345c4a0f07e609b112e0d1e`  
		Last Modified: Mon, 04 Jan 2021 18:54:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3404cbc204100a233c644769d2258363ef42728b2b65249f00a6381c0d981224`  
		Last Modified: Mon, 04 Jan 2021 18:54:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53008cf07e28bde16029d99717a07d47337cbaf6660d43e37656f718d32c4792`  
		Last Modified: Mon, 04 Jan 2021 18:54:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d38220b1d9b3910a8338deeabbff6fc709562a51aa8a175f2d240818f5e0bfd`  
		Last Modified: Mon, 04 Jan 2021 18:54:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ed7ecc9c3aaade2e2dda61d3568a7a512fe193757484925808d61b09fd7845`  
		Last Modified: Mon, 04 Jan 2021 18:54:04 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5f501c54b885524d72d6febc3751139fd1aae26b7066632df71bf30a120ad1`  
		Last Modified: Mon, 04 Jan 2021 18:54:01 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe61c4638d3f2f96f7be11b58a4373e9fd23c3fb3d8e3a122ed3a6eeb6ca5b02`  
		Last Modified: Mon, 04 Jan 2021 18:54:01 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6483c9d5ed09a140162450666395735b7af08fd5bb66a73bc7004e15607fa78`  
		Last Modified: Mon, 04 Jan 2021 18:54:04 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6e5b1f661cd44b57ecfd2a16acd79417331516a91d2cf59c8fa13b14d81f14`  
		Last Modified: Mon, 04 Jan 2021 18:54:02 GMT  
		Size: 300.6 KB (300640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc762e2db3ca03b6e2b9196012ac5a1380ebaa67274bf2f4936cf7cf6848adc`  
		Last Modified: Mon, 04 Jan 2021 18:54:03 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull caddy@sha256:52ba84b1bc620fe9c6bf5afbeb6047fe37f39a1e97df62101a2a162033c6e9dc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5800968218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae27b304e12044e887b0a87eaa663c7848bddab1fc3e1a583459e55499801b6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 13:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 22:53:08 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 04 Jan 2021 18:18:28 GMT
ENV CADDY_VERSION=v2.3.0
# Mon, 04 Jan 2021 18:19:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 04 Jan 2021 18:19:54 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 04 Jan 2021 18:19:55 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 04 Jan 2021 18:19:56 GMT
VOLUME [c:/config]
# Mon, 04 Jan 2021 18:19:57 GMT
VOLUME [c:/data]
# Mon, 04 Jan 2021 18:19:58 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Mon, 04 Jan 2021 18:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 04 Jan 2021 18:19:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 04 Jan 2021 18:20:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 04 Jan 2021 18:20:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 04 Jan 2021 18:20:01 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 04 Jan 2021 18:20:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 04 Jan 2021 18:20:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 04 Jan 2021 18:20:03 GMT
EXPOSE 80
# Mon, 04 Jan 2021 18:20:04 GMT
EXPOSE 443
# Mon, 04 Jan 2021 18:20:05 GMT
EXPOSE 2019
# Mon, 04 Jan 2021 18:20:46 GMT
RUN caddy version
# Mon, 04 Jan 2021 18:20:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c6d005eb9e78ad42f77f3dad7e29d954e78f0547f9884fe024a71f4042412970`  
		Last Modified: Wed, 09 Dec 2020 13:55:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d43cde540577a280266a838cfa13afe6a9cc3f995da2c60a9edbe76f85fc2`  
		Last Modified: Wed, 09 Dec 2020 23:00:17 GMT  
		Size: 10.1 MB (10058208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109fcea36e090f4ac505aa1c452e8d5d60d9eee531d8a9299906d87482770421`  
		Last Modified: Mon, 04 Jan 2021 18:54:44 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73d9d294f9237437e8528d7d489b5aff554a5f8c03de096ad3b52c3adfffc63`  
		Last Modified: Mon, 04 Jan 2021 18:54:50 GMT  
		Size: 21.8 MB (21794758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df1258484e4ac85a345320f37d96267b67becc244c8bbc12d40858e98ad4dc`  
		Last Modified: Mon, 04 Jan 2021 18:54:43 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e68ea4c0f30c1453ee98a4541d721ca832d2b51d4e1494d03865f21ddb2004`  
		Last Modified: Mon, 04 Jan 2021 18:54:43 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ebaa244b421120fd2af7f2c118eb15415ba90e2abde02e521454d45402c18`  
		Last Modified: Mon, 04 Jan 2021 18:54:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7497dae0c79efa2965863004e1362eef3d6a93edacee9d94fab613da6b74d3`  
		Last Modified: Mon, 04 Jan 2021 18:54:40 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db7860d239937431d5f35c76f33f73ea378b20f19483507c18e4c0127dccf68`  
		Last Modified: Mon, 04 Jan 2021 18:54:41 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5a2098ae1b5a7be1d84879c52cd6dda10f9cb96aa86854eb6353919be440f`  
		Last Modified: Mon, 04 Jan 2021 18:54:41 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a457307d576a96069a917c6a4e28967f3f35aec7daf05795e888bd516f93493`  
		Last Modified: Mon, 04 Jan 2021 18:54:40 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb2705d7ef08056ad743c530368007fee8db845419511a270438a833b5cee07`  
		Last Modified: Mon, 04 Jan 2021 18:54:38 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85371628953124d36c5fb909066bd97a77f6134a09d512f85f0ea1591fca2caf`  
		Last Modified: Mon, 04 Jan 2021 18:54:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949149af8be9d422128a7a40be8c9384eb00bed421e7c95f84dae2b9b26a399e`  
		Last Modified: Mon, 04 Jan 2021 18:54:37 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750dfb8234f081424e5627b2f8be1c65a967cbb9bdf65b08c18e1bc0fcc67f9e`  
		Last Modified: Mon, 04 Jan 2021 18:54:37 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6073c10f107869b2d81c6fddf8ce2abc7b8dab0f8656dbdbcaea00fe383406`  
		Last Modified: Mon, 04 Jan 2021 18:54:37 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc4ad8498ebee7beb5354ba2859817c99b2b69dfa523deb529659e5037c06e`  
		Last Modified: Mon, 04 Jan 2021 18:54:34 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55875c9c08b890c94d8bad2674b127f91363c695daaa7485fe20f95e989b0528`  
		Last Modified: Mon, 04 Jan 2021 18:54:35 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1d7565a7e2703bb0eaa1226a6a6d4142a9f4d3db67f36fb8514745585bc7b5`  
		Last Modified: Mon, 04 Jan 2021 18:54:34 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8ba21aee99c74983044cb5f8c011d7f28291494582222c330dc975a6ffd400`  
		Last Modified: Mon, 04 Jan 2021 18:54:34 GMT  
		Size: 250.6 KB (250616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb473eb3e7c9efb7d6d63fd81108daa1189d470c39355ecd4d621f68f815f242`  
		Last Modified: Mon, 04 Jan 2021 18:54:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
