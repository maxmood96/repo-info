## `nats:scratch`

```console
$ docker pull nats@sha256:80eb5023b4f9a6a43ccb90613913d8bbd7fb1d60ed202af2e7e7425add895c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6796429bd41a95837772476ae383c344688bbfa91067d66187cff0919bb9bff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262b07aad3ac9672f6fdfdafb0486d87b7afa1949afa2bab951305a9191f6e4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Jun 2021 04:22:05 GMT
COPY file:e739b42ab72b567be37f2b08b7cc64858dc247505c5f9065cbc349f3f7cde026 in /nats-server 
# Fri, 25 Jun 2021 04:22:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 25 Jun 2021 04:22:06 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Jun 2021 04:22:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Jun 2021 04:22:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4eead17c506be0458b8b300048220b15977a1fb9f1dabb07031134fe7cd321bd`  
		Last Modified: Fri, 25 Jun 2021 04:24:25 GMT  
		Size: 4.0 MB (3987827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71186d5a22ac8937ee584ce8ff166469d1d6e857b4bca58533fb852beaf49aff`  
		Last Modified: Fri, 25 Jun 2021 04:24:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
