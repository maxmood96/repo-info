## `traefik:maroilles`

```console
$ docker pull traefik@sha256:1fa3e9ee4509211196b926eb90d07ffbdf72d730ff3d8c428ac94f3b1c784783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:6eac900151c64c8465ef0e38b27d4ae9d877616230162279727337b47ff5dc08
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21584351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca551e784d546c33bab389a7b90aca0c74fa026194a34cbd4a6805a32fde606f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 15 Jul 2020 23:54:07 GMT
COPY file:dbebc61aa00cc3bd336b1fe611a0e32e7ad8b4b311e43c336de691d7c04a47af in / 
# Wed, 15 Jul 2020 23:54:08 GMT
EXPOSE 80
# Wed, 15 Jul 2020 23:54:08 GMT
VOLUME [/tmp]
# Wed, 15 Jul 2020 23:54:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jul 2020 23:54:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2668a1328cae473e5092f00bde31aa8d95bd00773bd3dbb5bf938539066ec41e`  
		Last Modified: Wed, 15 Jul 2020 23:54:48 GMT  
		Size: 21.1 MB (21125293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:201b3f9b283f6bc734fe33ab3c1c7c428d5878ccf4836be1892f1aea6bd63a9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20231475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cc1d1e27878e29edf1fc95fa792416065312621456b2f166e71de4782cae1e`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 15 Jul 2020 23:07:11 GMT
COPY file:185bd7cda9d632ce86c62da94a8061efac1291f616a72972fcda00ba82e29c4d in / 
# Wed, 15 Jul 2020 23:07:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 23:07:14 GMT
VOLUME [/tmp]
# Wed, 15 Jul 2020 23:07:15 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jul 2020 23:07:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eb8f091d88a8df352ff16fe91d7b9d4a458c1fbb7e28ce7a282293681e2c91`  
		Last Modified: Wed, 15 Jul 2020 23:08:16 GMT  
		Size: 19.8 MB (19772389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c98ea0955bb58f169837a6a29663ccec288bc496290aa06d19a63b1922ea44fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19952902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7f0e9591004fb0d9f0ec32c8b5e3294790b993e054cb774f1b08055583fcde`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Wed, 15 Jul 2020 23:30:24 GMT
COPY file:2004fb63ffb43df9c881281b0e9250dcd15332dde58681121ec9738221528602 in / 
# Wed, 15 Jul 2020 23:30:25 GMT
EXPOSE 80
# Wed, 15 Jul 2020 23:30:26 GMT
VOLUME [/tmp]
# Wed, 15 Jul 2020 23:30:27 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jul 2020 23:30:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.25 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100a118a37516ea44966052eb5d2b1de534be63dd7da7443bf69a60c4cf3731d`  
		Last Modified: Wed, 15 Jul 2020 23:31:38 GMT  
		Size: 19.5 MB (19493824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
