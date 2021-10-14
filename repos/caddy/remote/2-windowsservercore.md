## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:5f6f3a14bb0a50378a0cd54de891107bac8f133827f6dc90c42b80e46c477046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2237; amd64
	-	windows version 10.0.14393.4704; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull caddy@sha256:37896158024a0cd7f8e504de5834bc0948a7fcb436d17837926727e6fcef830c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698990436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a9fb6be636f6edeed7ef4425ed8cabb494140cdb230d40a85bc01cfe7d4e62`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 01:14:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 14 Oct 2021 01:14:56 GMT
ENV CADDY_VERSION=v2.4.5
# Thu, 14 Oct 2021 01:16:07 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.5/caddy_2.4.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('794fed88b38bfeb6b3b84d63f0887c4534fc3e94bd31173182b5af80fc7783beb41192bccffdb257a9bdf59541c6822a75fdbe714d65abc3c0cce9c02018eb82')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 14 Oct 2021 01:16:09 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 14 Oct 2021 01:16:10 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 14 Oct 2021 01:16:11 GMT
VOLUME [c:/config]
# Thu, 14 Oct 2021 01:16:12 GMT
VOLUME [c:/data]
# Thu, 14 Oct 2021 01:16:13 GMT
LABEL org.opencontainers.image.version=v2.4.5
# Thu, 14 Oct 2021 01:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 Oct 2021 01:16:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 Oct 2021 01:16:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 Oct 2021 01:16:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 Oct 2021 01:16:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 Oct 2021 01:16:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 Oct 2021 01:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 Oct 2021 01:16:21 GMT
EXPOSE 80
# Thu, 14 Oct 2021 01:16:22 GMT
EXPOSE 443
# Thu, 14 Oct 2021 01:16:23 GMT
EXPOSE 2019
# Thu, 14 Oct 2021 01:17:17 GMT
RUN caddy version
# Thu, 14 Oct 2021 01:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665e492ba7ee5015a57b1707f6f38dba54fce78ec0702f8835e1706514399f08`  
		Last Modified: Thu, 14 Oct 2021 01:24:39 GMT  
		Size: 359.9 KB (359912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532d778f3f718e6140d3f2de9eb7d33aa3267ad70d13e5ea5fbe4bb1b63f045c`  
		Last Modified: Thu, 14 Oct 2021 01:24:38 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99afa5426b255b06f2a82c61145df8a90321647affc7c641efe00d2b42cab78`  
		Last Modified: Thu, 14 Oct 2021 01:24:51 GMT  
		Size: 12.0 MB (12005028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51df745e088f94c24b04b4d8faef82a402c2ae93811d83de8b6b737b68815655`  
		Last Modified: Thu, 14 Oct 2021 01:24:38 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd6b823abc20a491415b3ad3ccb86e184b8757022155aafe3a00d3e5b7aba8c`  
		Last Modified: Thu, 14 Oct 2021 01:24:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37d72bdc456535a7412538f2f1c01d4d1a907ee0b7af55819ccd782206af365`  
		Last Modified: Thu, 14 Oct 2021 01:24:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c587c38fa9f8a899d8c107803db2a26352c7ef8b8b281c5270aaf07c34f003a9`  
		Last Modified: Thu, 14 Oct 2021 01:24:36 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317545f7f57cd1385761551bff772df090b607f90076a9a1bce67c329848ffd6`  
		Last Modified: Thu, 14 Oct 2021 01:24:36 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459153d69f0154ec005a34f57f04f406d38919f4e8fce54f760469e84cbd5c8c`  
		Last Modified: Thu, 14 Oct 2021 01:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec288065f33b8e19ccb8316615054fe365add7d30e6d21d3a049bde13ccda138`  
		Last Modified: Thu, 14 Oct 2021 01:24:36 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131878ddf4b2a9b6b6f38a59061c6eb85c7bd793fa42c57e85e04571915b2529`  
		Last Modified: Thu, 14 Oct 2021 01:24:34 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6592a859759d4788420489a41afb04e70312352ed860fe9eb6ba72c687d4d404`  
		Last Modified: Thu, 14 Oct 2021 01:24:34 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2d8cf2c2dfc078043ab1e659b8502c45028426c30098892f55eb8daa870208`  
		Last Modified: Thu, 14 Oct 2021 01:24:34 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bdb4e8b4b2c07da94a87cb734e0606f0136ad9d40cac2303f6a88971aabf41`  
		Last Modified: Thu, 14 Oct 2021 01:24:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da126f29e2f5ece2c4020d0f8b3ae3763d38fb1249abce185cd32bc7b16bc852`  
		Last Modified: Thu, 14 Oct 2021 01:24:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce3bce75862daf320e9ff55e02f555e8bc64248fb5794d744cbdb472e65aceb`  
		Last Modified: Thu, 14 Oct 2021 01:24:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed87969d5461009ef0a1ba9d56846bb0cd970c29d38ec932128fd23afbdb6b7`  
		Last Modified: Thu, 14 Oct 2021 01:24:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58527d3955c835addf2c00ee3268f54b59b56cc29c89d319f9b956dd2632b20f`  
		Last Modified: Thu, 14 Oct 2021 01:24:31 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197cd6167ed2ccd997de88375a9905b546713d9e237c8c5a1c45893010fa928e`  
		Last Modified: Thu, 14 Oct 2021 01:24:32 GMT  
		Size: 281.3 KB (281309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c66d6e66f26661a70297bebfdbf285d91eaca9d7b5490921a2404d35ad38d3`  
		Last Modified: Thu, 14 Oct 2021 01:24:32 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4704; amd64

```console
$ docker pull caddy@sha256:f671b5a7aa35e7645aeb45df5d62994b7515fe94618198a6a3e04c0abf7cf1b7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285485128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ea480541ba28016d87142fcf2c830601cfa21f17d53ac472d3535dbbe2a07`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 12:40:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 01:18:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 14 Oct 2021 01:18:36 GMT
ENV CADDY_VERSION=v2.4.5
# Thu, 14 Oct 2021 01:19:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.5/caddy_2.4.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('794fed88b38bfeb6b3b84d63f0887c4534fc3e94bd31173182b5af80fc7783beb41192bccffdb257a9bdf59541c6822a75fdbe714d65abc3c0cce9c02018eb82')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 14 Oct 2021 01:19:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 14 Oct 2021 01:19:54 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 14 Oct 2021 01:19:55 GMT
VOLUME [c:/config]
# Thu, 14 Oct 2021 01:19:57 GMT
VOLUME [c:/data]
# Thu, 14 Oct 2021 01:19:58 GMT
LABEL org.opencontainers.image.version=v2.4.5
# Thu, 14 Oct 2021 01:19:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 Oct 2021 01:20:00 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 Oct 2021 01:20:01 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 Oct 2021 01:20:02 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 Oct 2021 01:20:03 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 Oct 2021 01:20:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 Oct 2021 01:20:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 Oct 2021 01:20:06 GMT
EXPOSE 80
# Thu, 14 Oct 2021 01:20:07 GMT
EXPOSE 443
# Thu, 14 Oct 2021 01:20:09 GMT
EXPOSE 2019
# Thu, 14 Oct 2021 01:20:56 GMT
RUN caddy version
# Thu, 14 Oct 2021 01:20:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6974b1bd85ba3f9ce16d86231eced43f720fed9c13411d37584dfe7193bcde60`  
		Last Modified: Wed, 13 Oct 2021 13:27:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d982cd3ea4e0f39b0a59afe2410f4ac8f8ca8c9501681376105ac0756077aaf`  
		Last Modified: Thu, 14 Oct 2021 01:25:13 GMT  
		Size: 364.7 KB (364730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c9f99d5e17a16a8e02b7fbbdea0561d16844b94a78ba6b0a3980a1fd7ccba`  
		Last Modified: Thu, 14 Oct 2021 01:25:13 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a2f4b599c5a86a0efad9c64923ed92ef6348874f606dcc88d806a1bde65722`  
		Last Modified: Thu, 14 Oct 2021 01:25:16 GMT  
		Size: 12.0 MB (12047556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c9f9829b423db0615a1f5e60faea7e7acf6bbad919e96da1581aa1300b82ec`  
		Last Modified: Thu, 14 Oct 2021 01:25:12 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e587d5dec60023401a7b06bfef0515c714cc9c95f920fb6dc51ca92f79cacce`  
		Last Modified: Thu, 14 Oct 2021 01:25:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd530adf94358dba5c6504818a078b2c5f5838ee27b73ccb4209f28403a407`  
		Last Modified: Thu, 14 Oct 2021 01:25:10 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a2c0b803620763f4977aa22bf878b955b2dc925f4b9b983e8b9f3e37bca84`  
		Last Modified: Thu, 14 Oct 2021 01:25:10 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d1d61fbdd1784a524e400ef2f6adfd9082811c9e8e7c97a2117a1ecc3181b9`  
		Last Modified: Thu, 14 Oct 2021 01:25:10 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d36b7fbabf83c2f0a7c965b4f787a169f1f1295a04bc9c3c3fdbb0fd9ac968a`  
		Last Modified: Thu, 14 Oct 2021 01:25:10 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51195831e4cea58e85de48992766c2f7cc4cc6fd47a4a6fb3882c744bb36d21f`  
		Last Modified: Thu, 14 Oct 2021 01:25:10 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ca00fc7a8a309d40ce015c15098bb9d211cbc4c8336bf88a2c077116a9490a`  
		Last Modified: Thu, 14 Oct 2021 01:25:08 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92b1b6d340e40634655f50a50138549c6c70c61468789ae6e8429591ed449f`  
		Last Modified: Thu, 14 Oct 2021 01:25:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac818954f5a49435599cfcd5bccbc04eb575511eb8d8020f80d3f5b033162a`  
		Last Modified: Thu, 14 Oct 2021 01:25:08 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4463928f6dd92cd8b526d8451a040edeb1ff656c519f1130a19d65f08363dc68`  
		Last Modified: Thu, 14 Oct 2021 01:25:08 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da386c125ea3af7c5e43bdbd8734d5cd69492e04855043341345189a23a9c378`  
		Last Modified: Thu, 14 Oct 2021 01:25:08 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d5a5d0ff9b97c9797d980db55d78a43ddba8b84118c4af3fa0b6bc3bb9f6c`  
		Last Modified: Thu, 14 Oct 2021 01:25:05 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a877dc624ad3fc9873097f6de44c0fc79f308bca25337e4fa8169d0d6891b20c`  
		Last Modified: Thu, 14 Oct 2021 01:25:05 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d363765427e27a3693aed3fcc0d3ddf3228b7e01d320fb62d33f079a480c6e1a`  
		Last Modified: Thu, 14 Oct 2021 01:25:05 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b411941829ef681cc4a55bd5de5556631670b6d624eae094b6af3953ad7b1f`  
		Last Modified: Thu, 14 Oct 2021 01:25:06 GMT  
		Size: 281.1 KB (281088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f4f4d4d0b484cc3406a2b709d0f968cb33122ea0b7ff55885066024b4d7a3a`  
		Last Modified: Thu, 14 Oct 2021 01:25:05 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
