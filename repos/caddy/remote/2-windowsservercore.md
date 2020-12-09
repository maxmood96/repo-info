## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:94222b11fa710228c495d0963ae695e54d8e8e5ef631517a00f7e2557465e82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull caddy@sha256:b99f350b2de1665d145dad8c93c867427211ed43e1676b25da7c573bf24e97cf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416743592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242dc82d58b3eb28bad3e05fe3004a6da6c5748d32c08be14523fcafd480cbc9`
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
# Wed, 09 Dec 2020 22:50:43 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 09 Dec 2020 22:51:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Dec 2020 22:51:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Dec 2020 22:51:17 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Dec 2020 22:51:18 GMT
VOLUME [c:/config]
# Wed, 09 Dec 2020 22:51:18 GMT
VOLUME [c:/data]
# Wed, 09 Dec 2020 22:51:19 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 09 Dec 2020 22:51:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Dec 2020 22:51:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Dec 2020 22:51:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Dec 2020 22:51:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Dec 2020 22:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Dec 2020 22:51:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Dec 2020 22:51:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Dec 2020 22:51:25 GMT
EXPOSE 80
# Wed, 09 Dec 2020 22:51:26 GMT
EXPOSE 443
# Wed, 09 Dec 2020 22:51:27 GMT
EXPOSE 2019
# Wed, 09 Dec 2020 22:51:43 GMT
RUN caddy version
# Wed, 09 Dec 2020 22:51:44 GMT
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
	-	`sha256:914209fee7eb59b47ff4c4135d33f98b6b3af4209d114af2f9d0a8f65849d39b`  
		Last Modified: Wed, 09 Dec 2020 22:59:37 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493568bf34f325205007ec539e481c37dd13dd690c9e40e265f5a985393ba1a2`  
		Last Modified: Wed, 09 Dec 2020 22:59:43 GMT  
		Size: 16.3 MB (16325951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee88af8a1f1057877ee81813d03ca89698521e3a410830835be694de9aa3153`  
		Last Modified: Wed, 09 Dec 2020 22:59:37 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bfb8247c1f8c75fb59ee12dcd363fd2fcae2ac8da5e9fede5617faec7d082c`  
		Last Modified: Wed, 09 Dec 2020 22:59:37 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326e317e6021cafd340d9cb540564d2c79890682efe4baa10fe5bea17847adba`  
		Last Modified: Wed, 09 Dec 2020 22:59:35 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3769dc06e616a825c947d4d1a6c8aa5a427cf792adea55a9dc35672cc76b6d6`  
		Last Modified: Wed, 09 Dec 2020 22:59:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fa4f4d0eb978c7b41fb792c1faf3fc4823a131abc37ca7de8f13f2cb6b56d8`  
		Last Modified: Wed, 09 Dec 2020 22:59:34 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1042475d4dc01a2523d8dae43fd2096a6b87435d2f47f8c3275fcbac6d2453b`  
		Last Modified: Wed, 09 Dec 2020 22:59:34 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f1d1c1053e1fb4775c5939504f7c7554f3c65d033668836428b399f7bd3269`  
		Last Modified: Wed, 09 Dec 2020 22:59:35 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad4951dcfb5db6ad1ce8c0778b1647a8950ced04bd7b2b3051bf2b9df7209a4`  
		Last Modified: Wed, 09 Dec 2020 22:59:32 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dc0af1dcce3f75d580aaa3f73c92c6bd81249b0e86db979abe8ab511744095`  
		Last Modified: Wed, 09 Dec 2020 22:59:32 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223c49ff4855aff0e5bec5047249790dc3beef9bb99303c7963e0060e19c781e`  
		Last Modified: Wed, 09 Dec 2020 22:59:31 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db82d6aa5350a637ef41ced50f1e2aaab1876acadc50f289261c2b935251abda`  
		Last Modified: Wed, 09 Dec 2020 22:59:31 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ca7f7662411153b8d2e07b4e190fe5f28b55987e6c488eaf407f1b218757db`  
		Last Modified: Wed, 09 Dec 2020 22:59:31 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08ddd6fa1eec7ccc22299391dd16977f04c771c608d78aac09c2001b65cf36`  
		Last Modified: Wed, 09 Dec 2020 22:59:28 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11252ce2cac0c2d7e62754856c25a1fff65491437f664d589da9d70b608b18c4`  
		Last Modified: Wed, 09 Dec 2020 22:59:28 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159813c0e3aae77d0d2682fc6af3e2efa7204512c729017ee3c3282ba2a0ef30`  
		Last Modified: Wed, 09 Dec 2020 22:59:29 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a54bb1a8f7a905eb1774d7a6343ba5d306106c5dea74d1c9bd6e501cadcc86`  
		Last Modified: Wed, 09 Dec 2020 22:59:29 GMT  
		Size: 279.4 KB (279413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326eaebe45d7e1cadffa1215c3c58ff62541eba9a6209d0140f165099ca8d66b`  
		Last Modified: Wed, 09 Dec 2020 22:59:29 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull caddy@sha256:690a9e8ed59ad073fdf48712bad9bb8a3c942d100c4b379b3f01895905dada9f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5800848400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15cdc648fca30457ce53eff362d47ce02aebefe3e3869c7a67003cc9f3de197`
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
# Wed, 09 Dec 2020 22:53:09 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 09 Dec 2020 22:54:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Dec 2020 22:54:27 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Dec 2020 22:54:28 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Dec 2020 22:54:30 GMT
VOLUME [c:/config]
# Wed, 09 Dec 2020 22:54:30 GMT
VOLUME [c:/data]
# Wed, 09 Dec 2020 22:54:31 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 09 Dec 2020 22:54:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Dec 2020 22:54:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Dec 2020 22:54:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Dec 2020 22:54:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Dec 2020 22:54:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Dec 2020 22:54:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Dec 2020 22:54:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Dec 2020 22:54:37 GMT
EXPOSE 80
# Wed, 09 Dec 2020 22:54:37 GMT
EXPOSE 443
# Wed, 09 Dec 2020 22:54:38 GMT
EXPOSE 2019
# Wed, 09 Dec 2020 22:55:19 GMT
RUN caddy version
# Wed, 09 Dec 2020 22:55:20 GMT
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
	-	`sha256:3f1cb3aba27a86c6bfc96c6ee8f1778fc34c803d6a73e028b772f353bdaa1920`  
		Last Modified: Wed, 09 Dec 2020 23:00:12 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fba08ee40b5c7cc6bd794314039785636c387c33b03b6ae8804c82855546d4e`  
		Last Modified: Wed, 09 Dec 2020 23:00:19 GMT  
		Size: 21.7 MB (21688147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6bf11341a084f6e721ab3307d585db365feab3cafe5ccd13d3e45eaa825b6b`  
		Last Modified: Wed, 09 Dec 2020 23:00:12 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5652f1edbffbb90424a031a590be746b88955531f465e3171071cc861627cfdb`  
		Last Modified: Wed, 09 Dec 2020 23:00:10 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5879654d1ba873fbefe4d4f4cf04f4fc236c1b06355739aace87094aec7a247`  
		Last Modified: Wed, 09 Dec 2020 23:00:10 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7249d7e148d894abc47de261d624f605c263a6c5d33f946ab44cbf8508e801`  
		Last Modified: Wed, 09 Dec 2020 23:00:09 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705f17c7f16448f909172bb4ab2387cb8a9fbe53015f31945a485281b6780770`  
		Last Modified: Wed, 09 Dec 2020 23:00:09 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2518f043ac15f96f3d7209cd9ba09a011801e4893ee20b93e997894a7d05c`  
		Last Modified: Wed, 09 Dec 2020 23:00:09 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea0ee4a2384e36d3d715826e698e92ad2973d37760c3739c7f24c1d5b6e5630`  
		Last Modified: Wed, 09 Dec 2020 23:00:07 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a728aa2135880e4bda604c4f3dda7a805432c5020dcc5caa91cbca2bb1c1ebda`  
		Last Modified: Wed, 09 Dec 2020 23:00:06 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce4a1edefa2c1d049421764a2d56c2b6698f59cfeabcee1650f49af3a411c7`  
		Last Modified: Wed, 09 Dec 2020 23:00:07 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544505e4f2dca7871e19f148b8e5b0fcda661f26231146305a4117953193d15`  
		Last Modified: Wed, 09 Dec 2020 23:00:05 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e367b8829addd164fd7523883f9a4afaac2a45f397996f9f555dfc9f9efc787`  
		Last Modified: Wed, 09 Dec 2020 23:00:05 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6f338885dde1e48da16a2adea5f227ea93400f0bba92c5b26c19ce6c5ffdee`  
		Last Modified: Wed, 09 Dec 2020 23:00:04 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fec3499c9069ad73d1134ff56ae4bcfd60f542595684ffb5aab21094eaed8`  
		Last Modified: Wed, 09 Dec 2020 23:00:01 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9193a0ae2298ef7b30b475844d6b0ceafade168d507d7e310b8b5224461bf108`  
		Last Modified: Wed, 09 Dec 2020 23:00:01 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729f45a6315ae599187516f7d0dfbb7d855407b87648a38e0a53b4804f5cb319`  
		Last Modified: Wed, 09 Dec 2020 23:00:02 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9db07c0857db2b49c14d6c4dd764126c4945a573a5a3edb3b0278465f741c8`  
		Last Modified: Wed, 09 Dec 2020 23:00:03 GMT  
		Size: 238.3 KB (238322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6b684f9fb9937abcabf60ad70959f5344b4721c043ec4fa2cf21864d7af779`  
		Last Modified: Wed, 09 Dec 2020 23:00:02 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
