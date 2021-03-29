## `traefik:maroilles`

```console
$ docker pull traefik@sha256:104e0d832ae7a26f56d8f22c92df8a94cb4fbbbb2a6a4f50a710434c40145847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:e00ee616a3b242471dfd37fc4a47224500fb650d8472e80585bbce4af3758ff3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18137157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906db490f80d11b8292995bafb68f446c473a489529213f82847242ae262b9d0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:21:39 GMT
COPY file:7412e1ec4df789a7c412d984053a91d6cbcfa5e717664daefd86f56d52133131 in / 
# Mon, 29 Mar 2021 20:21:39 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:21:39 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:21:40 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:21:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd79ea7d84d34c942e13e7ef49f4d9b4d37a2c59fef618dc5ca44a93b5f66a`  
		Last Modified: Mon, 29 Mar 2021 20:22:35 GMT  
		Size: 17.7 MB (17697464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ef4135732d30c6209b85cf47d6ce104df48f6c9139fde1f2f3eb5925704fa62a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16957254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c73e8f22c4d8b96ece80d2d6e3b65ae6246aa2ae4f356615714c2a7e79768`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 24 Feb 2021 23:34:19 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 20:07:01 GMT
COPY file:021b5194c9f396ca24aaadd4ab3f8978febba7dff422827e0a613bb38224e5a2 in / 
# Mon, 29 Mar 2021 20:07:03 GMT
EXPOSE 80
# Mon, 29 Mar 2021 20:07:03 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 20:07:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 20:07:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e74b8526f2bdaa522f470d66d09f7ebbe9a1f060ce049ac91c0f7aad153e1be`  
		Last Modified: Wed, 24 Feb 2021 23:36:10 GMT  
		Size: 308.9 KB (308855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0c903ccfa53274059f2a4921657f10271ac6374b3f7f9094c4f026cc5a5b22`  
		Last Modified: Mon, 29 Mar 2021 20:07:50 GMT  
		Size: 16.5 MB (16517526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:58672e0711556e25704de4035eac1dd218ce82998a83986d912d4bff36aab0c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16538128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526c897fe43b070574d98f9135897eaa2106fc575b3cec56dc9f9b213cfe72e2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 25 Feb 2021 04:23:55 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Mon, 29 Mar 2021 19:52:36 GMT
COPY file:74c43ad3c5d71b75ac8726ad0ece7d7b6df15ddafbb3a2788809aba508d44be4 in / 
# Mon, 29 Mar 2021 19:52:37 GMT
EXPOSE 80
# Mon, 29 Mar 2021 19:52:38 GMT
VOLUME [/tmp]
# Mon, 29 Mar 2021 19:52:39 GMT
ENTRYPOINT ["/traefik"]
# Mon, 29 Mar 2021 19:52:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f74910073ee331bfbff1c3d20a2d29270f713f515ccee693e566b927d37654`  
		Last Modified: Thu, 25 Feb 2021 04:25:12 GMT  
		Size: 308.8 KB (308831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c77266db7cadaf81c6da0e1965473c18b40e57e28336f2a8741e83f19d269`  
		Last Modified: Mon, 29 Mar 2021 19:53:22 GMT  
		Size: 16.1 MB (16098424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
