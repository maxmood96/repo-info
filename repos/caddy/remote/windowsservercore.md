## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:96835edb2239b889b2a519d9b31159a2d525e342b2d4e651eb0afb3449b7aea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull caddy@sha256:b2206ce05b03bd8a17d6f95def3d7407f71a3278a49d48c41fca8ed43e69b632
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155606155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93883ca9602f6c7ee5e8d845b675d968ba9b50669a4aeffc3747dd6bf3abaa8b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 10 Jul 2024 17:13:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:13:14 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Jul 2024 17:13:15 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 10 Jul 2024 17:13:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Jul 2024 17:13:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Jul 2024 17:13:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Jul 2024 17:13:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 10 Jul 2024 17:13:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Jul 2024 17:13:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Jul 2024 17:13:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Jul 2024 17:13:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Jul 2024 17:13:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Jul 2024 17:13:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Jul 2024 17:13:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Jul 2024 17:13:32 GMT
EXPOSE 80
# Wed, 10 Jul 2024 17:13:32 GMT
EXPOSE 443
# Wed, 10 Jul 2024 17:13:33 GMT
EXPOSE 443/udp
# Wed, 10 Jul 2024 17:13:33 GMT
EXPOSE 2019
# Wed, 10 Jul 2024 17:13:38 GMT
RUN caddy version
# Wed, 10 Jul 2024 17:13:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e639a54269a6b039f9fce4663f19a389328aabe42186ead7761141f7419490`  
		Last Modified: Wed, 10 Jul 2024 17:13:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8154ab73bcef7704a09a335e20531a107b89720be6d48e058c9b73f18887c8f`  
		Last Modified: Wed, 10 Jul 2024 17:13:45 GMT  
		Size: 371.0 KB (371045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b197484f859b86359ec087a465763ebb633828616d8eaba25c42f91907cc8e44`  
		Last Modified: Wed, 10 Jul 2024 17:13:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e1079c1cf5cbf21448dd5918f991349457f6f70e8cbd89451072ff7b7ce992`  
		Last Modified: Wed, 10 Jul 2024 17:13:47 GMT  
		Size: 15.3 MB (15262837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3976ec4956416337b0878833be830b909dbcded911afc4bcc5dc49232e13d3a9`  
		Last Modified: Wed, 10 Jul 2024 17:13:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78cf229613c6ba61450e03307110d85563eee081ce993ffae17b9949e0c280`  
		Last Modified: Wed, 10 Jul 2024 17:13:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca0f6080f9f73614eb67d3748d41c309648b599dda306f09ba40407294cb9a`  
		Last Modified: Wed, 10 Jul 2024 17:13:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce84f11533ef1afafb72e428da54a9fef9662f223b20eb4bc877fb1313874dff`  
		Last Modified: Wed, 10 Jul 2024 17:13:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cadacbf999fce9e2937bf858e61ff46e78ccc2bd4e39f8965477cecc97ce84`  
		Last Modified: Wed, 10 Jul 2024 17:13:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b86a570d65847e988e66ef61bd1ef4449cd8be5899122b3a7aa927298c7581`  
		Last Modified: Wed, 10 Jul 2024 17:13:43 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32183475f7039cdd66f8170d777299fea1434f3605c25641d9a3ba1a62f9c07d`  
		Last Modified: Wed, 10 Jul 2024 17:13:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34708a8870f5e4b98b8416dd1a3b151c90ceaa400eb6dd1b8b77919650d1c1ef`  
		Last Modified: Wed, 10 Jul 2024 17:13:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf873bb050b323f199653c5cbe9dd19a0400015820302f438b486b3ffa03614`  
		Last Modified: Wed, 10 Jul 2024 17:13:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a089e86f5adc1d1652c27bde99eec529d1e1f89bfa1d6a3bb1f3d82e63b6e615`  
		Last Modified: Wed, 10 Jul 2024 17:13:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9563ab5c69403669147a072a19a42700901c76c4c65258b2beefe3a8fe2f7dec`  
		Last Modified: Wed, 10 Jul 2024 17:13:42 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e8694397435c044ebb904e26ee78ae8cdd2aed8f92119f6a5eb76099446d06`  
		Last Modified: Wed, 10 Jul 2024 17:13:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0888d815b81fdffa5451e15fc9d348a556774c160c970735e962320bc9015a`  
		Last Modified: Wed, 10 Jul 2024 17:13:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf8784d8f3d19d4047f913b2ee294c68da259ff427e6a267d8b7187a21c29f6`  
		Last Modified: Wed, 10 Jul 2024 17:13:41 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8a096054ccdd65b122e39c2f2b9bbef211a9b3e85409c35f478958f642bef4`  
		Last Modified: Wed, 10 Jul 2024 17:13:41 GMT  
		Size: 350.0 KB (350003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd654c6bb3733b7c3460705ec40749ed43d2e727d65405f13727a85a66b3fd7a`  
		Last Modified: Wed, 10 Jul 2024 17:13:41 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull caddy@sha256:3697474a43e0324944e1c082c684bc1da1878ee51789a90f204c8257b257e3a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2254614152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f92164b34d73ae8c5a6e888a316d46a9203fc69941705333c4b667267278fe`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:05:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:05:56 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Jul 2024 17:05:57 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 10 Jul 2024 17:06:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Jul 2024 17:06:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Jul 2024 17:06:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Jul 2024 17:06:24 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 10 Jul 2024 17:06:25 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Jul 2024 17:06:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Jul 2024 17:06:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Jul 2024 17:06:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Jul 2024 17:06:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Jul 2024 17:06:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Jul 2024 17:06:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Jul 2024 17:06:30 GMT
EXPOSE 80
# Wed, 10 Jul 2024 17:06:31 GMT
EXPOSE 443
# Wed, 10 Jul 2024 17:06:31 GMT
EXPOSE 443/udp
# Wed, 10 Jul 2024 17:06:32 GMT
EXPOSE 2019
# Wed, 10 Jul 2024 17:06:51 GMT
RUN caddy version
# Wed, 10 Jul 2024 17:06:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4108cac05f0f092715887a0fa11bd1fb41cd7d4b5b18d5235752c0a23046c774`  
		Last Modified: Wed, 10 Jul 2024 17:07:02 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fb27ca98bb0afb9c9b8866e8d8df54f8218cbbc44e7a86e508f23b72f326a6`  
		Last Modified: Wed, 10 Jul 2024 17:07:03 GMT  
		Size: 513.6 KB (513564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d767ee42de1825297d40eb982f32a6dcfcbe56551d8c8cad9637ebe848c0a5`  
		Last Modified: Wed, 10 Jul 2024 17:07:02 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7aeaba62a933ba8e6edfdbdaee8fe95f2b9a4bb9db5ee782e3c5789ee0e8696`  
		Last Modified: Wed, 10 Jul 2024 17:07:04 GMT  
		Size: 15.3 MB (15281586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d4ffea16f70c325faf4547daf28305c86da726413a5d5fd9a493b4008c95b`  
		Last Modified: Wed, 10 Jul 2024 17:07:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7167908047bff4de9753caa0cd4920f7fe4d9cd1752158e260f86f126187232`  
		Last Modified: Wed, 10 Jul 2024 17:07:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795da40290806f03d0f3eba609b21602b9d09d80af208e47d64c5ff0a55a7007`  
		Last Modified: Wed, 10 Jul 2024 17:07:00 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239d8baf75d4b9592dd94caa46621f65db97a5c3a9b90e9966a376a888c37f6`  
		Last Modified: Wed, 10 Jul 2024 17:07:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5b6f7a9e715341d5be90a7d87ad3b395783ef40077013f3b3098382c4f368f`  
		Last Modified: Wed, 10 Jul 2024 17:07:00 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58d97cee5a418d3bb7da632cddf53f0bc6d708d58d67ac182be9421b5a97844`  
		Last Modified: Wed, 10 Jul 2024 17:07:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb1d1ebe20c73ec27b55e9fb1c481283f6b88519ca15d1234f500f9f7d6ce3`  
		Last Modified: Wed, 10 Jul 2024 17:06:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efe79da11645ad68eac9474c866d7c8a4233bc38beeae329a87db6f79f1fea6`  
		Last Modified: Wed, 10 Jul 2024 17:06:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a178526a8755caa5aea86dc1e50d2dd6415757bfa43213747c36738b0dfb5f7`  
		Last Modified: Wed, 10 Jul 2024 17:06:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0da87227ed99caafe7485bd3320ce36de32e226762c99684ab80cc0e40881ce`  
		Last Modified: Wed, 10 Jul 2024 17:06:58 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ade48a4b97e7789b6c1fffeac97089983b08a88cf71b84fc176d46755e3063b`  
		Last Modified: Wed, 10 Jul 2024 17:06:58 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4faba4f7b803e9189307726935be59cc237afa88dc768881cc0260ad3102ee7`  
		Last Modified: Wed, 10 Jul 2024 17:06:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110728c04e88d6b574c31ad5014a76085d29e7ae84eb965ec46e69a7cd8002ab`  
		Last Modified: Wed, 10 Jul 2024 17:06:56 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3db3b7f535ab200265b63244bd24d42f4edfc07e8bb51f932277d97d6b728f`  
		Last Modified: Wed, 10 Jul 2024 17:06:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1142a84fa475534697516120afdb8a6c6e4674e73ddf8e0517704ec5bc94b2`  
		Last Modified: Wed, 10 Jul 2024 17:06:56 GMT  
		Size: 367.6 KB (367552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08c5d7a23f4743ecf91b3452b2f94d7f6f912aee614e0fcacdd5078718612b6`  
		Last Modified: Wed, 10 Jul 2024 17:06:56 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
