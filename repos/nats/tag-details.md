<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.22`](#nats2-alpine322)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-ltsc2022`](#nats2-nanoserver-ltsc2022)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-ltsc2022`](#nats2-windowsservercore-ltsc2022)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.22`](#nats211-alpine322)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-ltsc2022`](#nats211-nanoserver-ltsc2022)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-ltsc2022`](#nats211-windowsservercore-ltsc2022)
-	[`nats:2.11.15`](#nats21115)
-	[`nats:2.11.15-alpine`](#nats21115-alpine)
-	[`nats:2.11.15-alpine3.22`](#nats21115-alpine322)
-	[`nats:2.11.15-linux`](#nats21115-linux)
-	[`nats:2.11.15-nanoserver`](#nats21115-nanoserver)
-	[`nats:2.11.15-nanoserver-ltsc2022`](#nats21115-nanoserver-ltsc2022)
-	[`nats:2.11.15-scratch`](#nats21115-scratch)
-	[`nats:2.11.15-windowsservercore`](#nats21115-windowsservercore)
-	[`nats:2.11.15-windowsservercore-ltsc2022`](#nats21115-windowsservercore-ltsc2022)
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.6`](#nats2126)
-	[`nats:2.12.6-alpine`](#nats2126-alpine)
-	[`nats:2.12.6-alpine3.22`](#nats2126-alpine322)
-	[`nats:2.12.6-linux`](#nats2126-linux)
-	[`nats:2.12.6-nanoserver`](#nats2126-nanoserver)
-	[`nats:2.12.6-nanoserver-ltsc2022`](#nats2126-nanoserver-ltsc2022)
-	[`nats:2.12.6-scratch`](#nats2126-scratch)
-	[`nats:2.12.6-windowsservercore`](#nats2126-windowsservercore)
-	[`nats:2.12.6-windowsservercore-ltsc2022`](#nats2126-windowsservercore-ltsc2022)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.22`](#natsalpine322)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-ltsc2022`](#natsnanoserver-ltsc2022)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-ltsc2022`](#natswindowsservercore-ltsc2022)

## `nats:2`

```console
$ docker pull nats@sha256:7971c76fcd4057c090faf5bc7673199ffe0ae586704518e9a469f156155b4e47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4893; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:c1379a8588df47244a4789ede85e8ae7490bd37006bde837e4d6fb6f559cb0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:f55092a58ef4b6883fd9b9e67c8741139c3701acff2d7e57930abbb54d2d4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10886061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81529466020c291e5ad80f56987ed653d491e1b9476ccbdeaf67b72affa3c278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8887a98e8249b73b0777bfbc8c0a30b02d3c21e3c39a9d768c5871b5585777`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 7.1 MB (7080215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dead58ebc17268f1b2f4cec215f560e3a07cc610d28eeff77d5f1c5d8e2517`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b4cd24f67b5d5afe059593810655b6887ba69dbdb160f71907e3daca8a8dc`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:685e730f881ec97c5e115e96bfe8066a26a611e53bcbfa4f0e69d4b4a174b46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb00ece4ca5cf51cc4d452e9249450fed5b54cfe2a9112947dca28d2ea8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3ba67a28104834d1d93b1e7e33ff17be9085f62d4b1100860816af7c9e0de`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c7bf3f984b3b64f0c1f9f4674a8f76c32e17a58c3a69291ad03b749fb8275ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52985b6ab22ea9e18f31378c7d723405b36c8533ab7e35049e80e606ec5042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148f12e063d142770b6e05b9f9c2ab014ab5763dff5f40cf43b4d8741dea20e0`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 6.8 MB (6797772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb32797a1c1b66b3d5d82193923eb3b39bbd560af58c01e71d7f46127eda32c`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c38be02f7f6968455354dfe4a4a05e5f20fbcdad07b63a3add2b522b3fc163`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7f5278fc819e312da44d7f8c6548fbd4f008b7047b81aaec0c88e1b6e7bf80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf1a9035fbf11bd94daf97ff6446b8c962f779e52915fdb47f723375a90161`

```dockerfile
```

-	Layers:
	-	`sha256:d069f32f6e0103cf7962bc3e50c1be2b0953ab9edcfb7db9f63defe80ce6c7b2`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de66d6fac8ce8ebef0e1032f68c75720b2d9fe3a040132c69bce4613ae04a5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10016287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb89708d609d7d7c02e11f18dbd6f2ebbd095aee4402d8d2d9a9c4ca7917e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627631ba1918c54c7a3365b569389ba221a3fcbd467f2f68c02834aa91cc94f`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 6.8 MB (6791688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909a283e1b0f458613bac969dccdc3e622f3167995890a9b73344d1afe42e0c`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc1d6c83015eb80bc6e00a18fd3fe4b50483b56a1b8d381db8551986ad949e`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a89cb4125128c4481995506bc126626436c2a4398b4d1ca640b05c513c9c3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576436877db30f3cde211a66a4c4013292cae5b6f4cdcba857a0f440e84397a8`

```dockerfile
```

-	Layers:
	-	`sha256:c681f3aa2919334b313a7f825221815da8a74b0c5717aece45a141747c4666a4`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ce72c5047aac010d13d69e087e2ef792ba483b581d3fe131a06f24f4bcd64499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10629509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78db93426f4ce81493b1740958536016471acce7c2469d30642d1ce5e2505028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825bb7632b2910036c4e99446261eaccf38a5407182667a9a5544165b29a3a66`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 6.5 MB (6489020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a075238f2783d207491918f497c4935823239fef8402991a1501e453f6dba`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e51ee93c455d52b0a680fe79d12a069061e5d506026beeda5e511a4b3221a49`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6803835c0dc24ce636ea74af20236401d626a7086072c838f1bdc957a100b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389309d70c5e974ba909c72462ccaecc37686be93ec78f5b3f4ec005cb0760b`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a9525024c9f083b6bf1027d0683e9da385aa15944aa3dd296418810f297b6`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:ea21e6eb9baed3f48d70928e28581f139ea88123ae96c10ab7fd753b196f711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6294e924a35b3ba351e1a9cb918458e4656b4bf790282e9b5b571ef60785615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:50 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f47dcf083e6405dbb62b78c40e89eddfa579782e18796398d04ac483723b67`  
		Last Modified: Mon, 09 Mar 2026 20:26:00 GMT  
		Size: 6.5 MB (6538200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cff225f6b222724626788da2eb98a26c2385e0464e86d59d843ae8cd9131b`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264d913d41a7e5acf68f5c7336a947d1c985b3beb40308165f5e1529c5e7e1`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c395e1e7cdcf166da464ce9b176a78f41cc1e379d12029384d18535e7510dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd1e702aa11e4a3b35ba6f6d3a008217124ef4d19d93d23e12767750a22642b`

```dockerfile
```

-	Layers:
	-	`sha256:1eed2a8cf66e0339f0d26be0f99591e27aa134d22ad734dce841c59737673453`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:922a66519e1e1d9166fcdf6ffc4ee018befd6cde9b8b53d7e614d2e41ed770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a50c0d0127f61de22b52cfc3acbf5c208e15f76b7a6e18a51e075465786d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:21 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a6cdb957401649789e5b4f2cbe88f55a7b8e0a8bd0609c92d9eef2c3a417e`  
		Last Modified: Mon, 09 Mar 2026 19:01:30 GMT  
		Size: 6.9 MB (6920512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7111270df9c5fff857ec52c3ba39df86a8800642c13f0d00bd04a1712b9d4e0`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919a6d79781833003c5f530b73820bdd56e515c4670f1a782d6f68bd6cbaf8d`  
		Last Modified: Mon, 09 Mar 2026 19:01:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dd1073397e51e35ad7dd3e192c8a292dede602bcea951e4d02a8e2acc25cc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f173e09372d1c0d616aa2b5e814f124a00b622196f5122bbe8ceb997b7f93d`

```dockerfile
```

-	Layers:
	-	`sha256:f149e96bc2411d24ddb1f3bd40351a3b5649c09c2f17f7db57ca653a6e4731ee`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:c1379a8588df47244a4789ede85e8ae7490bd37006bde837e4d6fb6f559cb0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:f55092a58ef4b6883fd9b9e67c8741139c3701acff2d7e57930abbb54d2d4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10886061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81529466020c291e5ad80f56987ed653d491e1b9476ccbdeaf67b72affa3c278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8887a98e8249b73b0777bfbc8c0a30b02d3c21e3c39a9d768c5871b5585777`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 7.1 MB (7080215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dead58ebc17268f1b2f4cec215f560e3a07cc610d28eeff77d5f1c5d8e2517`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b4cd24f67b5d5afe059593810655b6887ba69dbdb160f71907e3daca8a8dc`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:685e730f881ec97c5e115e96bfe8066a26a611e53bcbfa4f0e69d4b4a174b46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb00ece4ca5cf51cc4d452e9249450fed5b54cfe2a9112947dca28d2ea8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3ba67a28104834d1d93b1e7e33ff17be9085f62d4b1100860816af7c9e0de`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c7bf3f984b3b64f0c1f9f4674a8f76c32e17a58c3a69291ad03b749fb8275ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52985b6ab22ea9e18f31378c7d723405b36c8533ab7e35049e80e606ec5042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148f12e063d142770b6e05b9f9c2ab014ab5763dff5f40cf43b4d8741dea20e0`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 6.8 MB (6797772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb32797a1c1b66b3d5d82193923eb3b39bbd560af58c01e71d7f46127eda32c`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c38be02f7f6968455354dfe4a4a05e5f20fbcdad07b63a3add2b522b3fc163`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7f5278fc819e312da44d7f8c6548fbd4f008b7047b81aaec0c88e1b6e7bf80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf1a9035fbf11bd94daf97ff6446b8c962f779e52915fdb47f723375a90161`

```dockerfile
```

-	Layers:
	-	`sha256:d069f32f6e0103cf7962bc3e50c1be2b0953ab9edcfb7db9f63defe80ce6c7b2`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:de66d6fac8ce8ebef0e1032f68c75720b2d9fe3a040132c69bce4613ae04a5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10016287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb89708d609d7d7c02e11f18dbd6f2ebbd095aee4402d8d2d9a9c4ca7917e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627631ba1918c54c7a3365b569389ba221a3fcbd467f2f68c02834aa91cc94f`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 6.8 MB (6791688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909a283e1b0f458613bac969dccdc3e622f3167995890a9b73344d1afe42e0c`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc1d6c83015eb80bc6e00a18fd3fe4b50483b56a1b8d381db8551986ad949e`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a89cb4125128c4481995506bc126626436c2a4398b4d1ca640b05c513c9c3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576436877db30f3cde211a66a4c4013292cae5b6f4cdcba857a0f440e84397a8`

```dockerfile
```

-	Layers:
	-	`sha256:c681f3aa2919334b313a7f825221815da8a74b0c5717aece45a141747c4666a4`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ce72c5047aac010d13d69e087e2ef792ba483b581d3fe131a06f24f4bcd64499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10629509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78db93426f4ce81493b1740958536016471acce7c2469d30642d1ce5e2505028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825bb7632b2910036c4e99446261eaccf38a5407182667a9a5544165b29a3a66`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 6.5 MB (6489020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a075238f2783d207491918f497c4935823239fef8402991a1501e453f6dba`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e51ee93c455d52b0a680fe79d12a069061e5d506026beeda5e511a4b3221a49`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6803835c0dc24ce636ea74af20236401d626a7086072c838f1bdc957a100b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389309d70c5e974ba909c72462ccaecc37686be93ec78f5b3f4ec005cb0760b`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a9525024c9f083b6bf1027d0683e9da385aa15944aa3dd296418810f297b6`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ea21e6eb9baed3f48d70928e28581f139ea88123ae96c10ab7fd753b196f711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6294e924a35b3ba351e1a9cb918458e4656b4bf790282e9b5b571ef60785615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:50 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f47dcf083e6405dbb62b78c40e89eddfa579782e18796398d04ac483723b67`  
		Last Modified: Mon, 09 Mar 2026 20:26:00 GMT  
		Size: 6.5 MB (6538200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cff225f6b222724626788da2eb98a26c2385e0464e86d59d843ae8cd9131b`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264d913d41a7e5acf68f5c7336a947d1c985b3beb40308165f5e1529c5e7e1`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c395e1e7cdcf166da464ce9b176a78f41cc1e379d12029384d18535e7510dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd1e702aa11e4a3b35ba6f6d3a008217124ef4d19d93d23e12767750a22642b`

```dockerfile
```

-	Layers:
	-	`sha256:1eed2a8cf66e0339f0d26be0f99591e27aa134d22ad734dce841c59737673453`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:922a66519e1e1d9166fcdf6ffc4ee018befd6cde9b8b53d7e614d2e41ed770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a50c0d0127f61de22b52cfc3acbf5c208e15f76b7a6e18a51e075465786d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:21 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a6cdb957401649789e5b4f2cbe88f55a7b8e0a8bd0609c92d9eef2c3a417e`  
		Last Modified: Mon, 09 Mar 2026 19:01:30 GMT  
		Size: 6.9 MB (6920512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7111270df9c5fff857ec52c3ba39df86a8800642c13f0d00bd04a1712b9d4e0`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919a6d79781833003c5f530b73820bdd56e515c4670f1a782d6f68bd6cbaf8d`  
		Last Modified: Mon, 09 Mar 2026 19:01:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:dd1073397e51e35ad7dd3e192c8a292dede602bcea951e4d02a8e2acc25cc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f173e09372d1c0d616aa2b5e814f124a00b622196f5122bbe8ceb997b7f93d`

```dockerfile
```

-	Layers:
	-	`sha256:f149e96bc2411d24ddb1f3bd40351a3b5649c09c2f17f7db57ca653a6e4731ee`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:4381ef3a8a655e7f0cca77861aa1b12801161df68c13147da4629b7bbdc1201e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:4e65924c3379e91937053a1f79ed9a3a79bf8a7bb5b38caca931059d70656eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4e65924c3379e91937053a1f79ed9a3a79bf8a7bb5b38caca931059d70656eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:4381ef3a8a655e7f0cca77861aa1b12801161df68c13147da4629b7bbdc1201e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:9b0bc6e81344da3bd2751cf47d851dc71c28a7d7d30f7328b435c0d5083f3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:6ae257bf95b984fb32a4f6eeb280e11b127a5779eb61c1e4d2054e1163e39a06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989938833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf972a8f9ff2fce9f9ca75a08b35c399345e0347c096de0b4f53579fa7ad32d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:58:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 21:58:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 21:58:11 GMT
ENV NATS_SERVER=2.12.5
# Tue, 10 Mar 2026 21:58:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Tue, 10 Mar 2026 21:58:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.5/nats-server-v2.12.5-windows-amd64.zip
# Tue, 10 Mar 2026 21:58:14 GMT
ENV NATS_SERVER_SHASUM=29d6eca9ce085731bd63b32eeff7fae076938d31dd095acccfc70f2496d07ea7
# Tue, 10 Mar 2026 21:58:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 21:58:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 21:58:54 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 21:58:55 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 21:58:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 21:58:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04c32730da76e4f8c0992e8486404cface27cdbf86a7fe00437d3025590b7e`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02ad44b5ae354c11458cd62dee34cf93d9389058036580d4260d9551883ed0`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d2d6023a53e21e129bd012c45fed3f50dabc9d0bcea695e14ecdac1ad3f03`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0deaad7f12bcdc5138b621c8a8c2a35766f41f719b51f6add6f71d28a0842`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2a17f84ab038fcc41ab1c8aa33270d582ed981327779baf6d26e85c36b1f1c`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800dc056e1954416cde33967232d04ac013a4b298a04c3bb591bb6cda1a3696`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b556c3513211380357d8ba1d5774644200201d0a0973350c0b338eb7aecc6a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 484.7 KB (484712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e93160909732ff5d08e605284a33be5e2f51dd89a8ed9b5ad40bd5948a090`  
		Last Modified: Tue, 10 Mar 2026 21:59:04 GMT  
		Size: 7.2 MB (7159095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b56e0af4952401a1d938512f31f1e379baf7f63ec96da79f873f8cdf83c397`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d839d11021d15ecfbce6ae4d506186302258eabf46c50e87ce5c5b75ff02a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f70edc90f77cbdf7689415400d2da65bb2e9a269a97c7411d32ace56cba1ff`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5573ab3f95d8693954515f4dfd4b0a086da95b6c7456f05348de2e4c1eee1a2`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:9b0bc6e81344da3bd2751cf47d851dc71c28a7d7d30f7328b435c0d5083f3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:6ae257bf95b984fb32a4f6eeb280e11b127a5779eb61c1e4d2054e1163e39a06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989938833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf972a8f9ff2fce9f9ca75a08b35c399345e0347c096de0b4f53579fa7ad32d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:58:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 21:58:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 21:58:11 GMT
ENV NATS_SERVER=2.12.5
# Tue, 10 Mar 2026 21:58:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Tue, 10 Mar 2026 21:58:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.5/nats-server-v2.12.5-windows-amd64.zip
# Tue, 10 Mar 2026 21:58:14 GMT
ENV NATS_SERVER_SHASUM=29d6eca9ce085731bd63b32eeff7fae076938d31dd095acccfc70f2496d07ea7
# Tue, 10 Mar 2026 21:58:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 21:58:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 21:58:54 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 21:58:55 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 21:58:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 21:58:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04c32730da76e4f8c0992e8486404cface27cdbf86a7fe00437d3025590b7e`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02ad44b5ae354c11458cd62dee34cf93d9389058036580d4260d9551883ed0`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d2d6023a53e21e129bd012c45fed3f50dabc9d0bcea695e14ecdac1ad3f03`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0deaad7f12bcdc5138b621c8a8c2a35766f41f719b51f6add6f71d28a0842`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2a17f84ab038fcc41ab1c8aa33270d582ed981327779baf6d26e85c36b1f1c`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800dc056e1954416cde33967232d04ac013a4b298a04c3bb591bb6cda1a3696`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b556c3513211380357d8ba1d5774644200201d0a0973350c0b338eb7aecc6a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 484.7 KB (484712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e93160909732ff5d08e605284a33be5e2f51dd89a8ed9b5ad40bd5948a090`  
		Last Modified: Tue, 10 Mar 2026 21:59:04 GMT  
		Size: 7.2 MB (7159095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b56e0af4952401a1d938512f31f1e379baf7f63ec96da79f873f8cdf83c397`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d839d11021d15ecfbce6ae4d506186302258eabf46c50e87ce5c5b75ff02a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f70edc90f77cbdf7689415400d2da65bb2e9a269a97c7411d32ace56cba1ff`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5573ab3f95d8693954515f4dfd4b0a086da95b6c7456f05348de2e4c1eee1a2`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:ca470f029ee01dc120305c4e1dfb7d569b15994ea26a7ed3793d650b9087cf08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:49c32c87bec99746a8b30c2f1b4f75b4f523e229449735b31fb0a862955b5d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6489015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84937fc8d4b2ea427a9288296a8e1550d90adfd678004ec184ff891d05194455`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:44 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:01b31e3d8e4b92d54d5280ce1923156df749289333050774805f4ee3d6604985`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.5 MB (6488506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7736bcae51bba47854c82d0063b92a3a61826af7e6dadba0def0eab42726b14`  
		Last Modified: Mon, 09 Mar 2026 19:12:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:9c07ccf3d70484b44c3828d9555784bf274d430d92ede4d1796c21d0be998585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1c288b1e85e54be02734d0b651cd0b3d32b72627aae2f30ead31f99652e273`

```dockerfile
```

-	Layers:
	-	`sha256:5af6cc00e9a512cc3c76556ae551449e273f48c36c6e44964d7c72d8f0cabfea`  
		Last Modified: Mon, 09 Mar 2026 19:12:49 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:925f78234d1ac10f9228b170aae2705acc585485e468496eaa76eb6d4eeeac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667802c2ce4b89d852e3b146d8806596bb57115022ff32978e8232c29f668a4a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:32 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:32 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:32 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a7277d8d113dec8b315d7940efa55fb3c3a6e91626be07e09fabffdb888af61`  
		Last Modified: Mon, 09 Mar 2026 16:09:45 GMT  
		Size: 6.2 MB (6212623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd98f25d5ef9e8bf9b99604eaa363092b8f7500f9c127cb6e7b0cd93a64f062`  
		Last Modified: Mon, 09 Mar 2026 21:49:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:2f0e8526bcb8e60bfd9c305adc9a3a520763f0c9cab98b74b6b93c30f0e3749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6eb54dc8f395b0cd2162dbffc902620efc9011f71a7f9acce9ba1ee40516349`

```dockerfile
```

-	Layers:
	-	`sha256:acadba40a6f29e93baf61c470cc428238af6e70b7a768143a5bfa122463d7698`  
		Last Modified: Mon, 09 Mar 2026 21:49:36 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:8168117cee667bc4d9f9e684c1f2324c54fcb6c873ee8e6253acf0e904550135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ebc16f64dc50aed83704d38077d99f7c19b9da02a0cfa81260db2f81009ce4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7960b0843dc07a38a4f69f7d3ae72c7e4c393207293594028277c1c6fa469cc5`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.2 MB (6205764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a5c7f1d5f5c1920740cf15921f65d41e3220fc251e3511dfc6ae3e9531d737`  
		Last Modified: Mon, 09 Mar 2026 21:53:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:127f56764c95373649dfb4b00ce4e03a80a82af31ae70b87e489b2fb1c70ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c11a7cb933860a45f2843890d2e4b8349abedea08888d133122e68f037f8e30`

```dockerfile
```

-	Layers:
	-	`sha256:56f907fa91fdd38de99f07a9e06a9c6f02ca279b0dc5842384a8adca4d5fa4a8`  
		Last Modified: Mon, 09 Mar 2026 21:53:18 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f153f55bb9f5e7c1eea5420d42a96c289a0f00006c2dd87aca1bbbfa130b14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5909462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a671f51ee515bfccdbbda9704f971ce62d649d92ed07a09c52ea3e585338668`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3e32192681ac27bc253f38f45ca0d5b2ad36ba165acc96342765c068290a3796`  
		Last Modified: Mon, 09 Mar 2026 16:09:45 GMT  
		Size: 5.9 MB (5908952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261d013df878cf62dac4f23852a22ce188b63518350e086e2d9caee1e9aef7`  
		Last Modified: Mon, 09 Mar 2026 19:12:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:35e1227b1a8949f792c6fa82a6ff1d0c3ee628f5b851524df86d4361f04c1684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44ab2b9d0255e052be33a525127dff84a7af1da36ccd121c82f7c61a7270cf1`

```dockerfile
```

-	Layers:
	-	`sha256:b5e81d8bd95602e874a18e803af3066a1a40ab909c35b9889aa58ebc23002ef3`  
		Last Modified: Mon, 09 Mar 2026 19:12:27 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:dd35dbfa99c5fcec2325bc24647f409ac503e74f8e37872006b7ae01540ec802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a180d825c868c7c0dc0e087a116313a4844d95f6474e36d0c1b42ec66c1b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7db64218ee876daffe3f2d1117157a1265b22c9cf8500c591c02d8cf2157b901`  
		Last Modified: Mon, 09 Mar 2026 16:09:42 GMT  
		Size: 6.0 MB (5958115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a656cf595bc0cf59dda8f8a382852db660e89b23335bdc816f62ba7917cfe65`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:dd21301252bd4aa3ff3fc7021490740066e3017782a31ae4134c26884fec95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56459d873e6b8b8442c8994c72f4a757c4a21b973448ba17883850c1acc46e3`

```dockerfile
```

-	Layers:
	-	`sha256:a1e5736bab434f9ed5f26403ff3ebf6d0d8f1eb29a91344a829ac31cb6ea136f`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:17c0134c00f91e8f138a33efbc730597da0f1520b705428d2d35ef9ec55e885a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a714c69afcbf633ec367b366c5ffaea6a256b35510b878c49731e45c0daad6ae`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:16 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84d2ac1d4fe9a738e55809ec9f070c1f06c8941abb334c06b7269033719fa09b`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.3 MB (6329356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ca2e0276ecac592aba65dfafef7bb374ad3533206f35178cd658c0a6801d67`  
		Last Modified: Mon, 09 Mar 2026 19:11:24 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:18aad3846a8d8b263b848d12942c0e669493d6e3d5e171fc8b5edfc4a731cf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e7663af8889626ff642c6b24a89ec101e0afc0f8fb225d7a6cc33df5b4a91`

```dockerfile
```

-	Layers:
	-	`sha256:6b7de3173d9fdb8824cded52df758f8a406c8168c7b839e77e641ad60b73d732`  
		Last Modified: Mon, 09 Mar 2026 19:11:24 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:cb62597c55ed0e4879a76d7954dcfe510e9ae2c407ef07d7f6162cb1e546ea6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133324190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb885af05de0690a25ffe5ed510dd7780920301fa4f8409a563709978406036`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:37:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:38:01 GMT
RUN cmd /S /C #(nop) COPY file:690296852f806393ad867a961bb2117053cdde9e33cb62cfc133cf2222b12dde in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:38:02 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:38:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:38:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:38:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe9bc4bba5a63f8196fe0b5ef4ad39026bb53e1400380d906e8ed27489d49a`  
		Last Modified: Tue, 10 Mar 2026 22:38:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3dff46f73915f0c1b07ff70feb495b9fc958f0feb4e98841dd5893831f63b6`  
		Last Modified: Tue, 10 Mar 2026 22:38:09 GMT  
		Size: 6.7 MB (6667782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cdf89affe03acb92a2a6462b75875142d25904087ee6ef04a352a05ac129d7`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2309fea759ab93e8e58a8eaf26bd7f55af17ac581cd812227437bded0e1088`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540a38924fe9c502f31944994dcba191d8e58b7ac043443f22fe21bc664fa0b3`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71528307feff7f868710b39b8b35d3859481c3c704074a90356625664fdd9243`  
		Last Modified: Tue, 10 Mar 2026 22:38:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:58ebbf8180181c2d581488c720ec9bd5fd7455916d0ed7cc64df305a618adca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:b0c37fffebabe483f975db48af95c240c8d108c1dd1dc3862e88f0147f369819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10752953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d25602f9385026b3db3fb35d2eedf14d53ef200ee624d741f5acc1f6b6bf69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:41 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:34:41 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:34:41 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:41 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f00b7901d8dee0560a03078f612f2cb3413aeddef2accf6482b430a82879db`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 6.9 MB (6947107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af7185d097383bbf95a4d1d24f5faf9e2f2cb92b4e5059268de4b7c9f0e3e5`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e325fad7fcbdb59dc485bf150a3a7453802f095e111db6d81c320dd55d656dd`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a6501e31f32a154a85a64c2f212c464f81b702cee6d27e15fef26fb8f6544750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee9915f808e75fc71c73d5f98392a42bf85bdef9a436b6b6d7227946f8b2b8d`

```dockerfile
```

-	Layers:
	-	`sha256:0f6408ec8cf247b2de3f55f1ec74aaa58cbfa4fc89316cd9670e23a999700d77`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:771bf4346560cfb3d930014ac3fbf5186aa662ecfc9645f98d4c57e018a59cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10178135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e374b2e6ac4595c12866b39853a121ce0072c732a6d3999c924e5ed712d2f17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:42 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:48:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:48:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6475bea2ea18d0283bcf65bee880a4f50ab166ed503ead4d039037781e0e726`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 6.7 MB (6672120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966e5bc2ba77ffdb050c8a28a0b18e6c0662b211602eb7a7895ff3846c8ed549`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c866a98f69ad961fc3f0ed0d66124b9c020dd64bcd898032a6b54620fc4db3f`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:002d5873835f745f6e8179fd77bb0341743724bc64c06a314767f5932d836311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4562dc25f9df3852ff268d05036f470baaa595febdb93a0b81815a8c1aa94a`

```dockerfile
```

-	Layers:
	-	`sha256:b0991311b20547169d644dbeec09e5adb2d667f9304d10c3efbcdc7e0b188db3`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9c1eb92bafe472b4b8b57140a21b74bbe7518eb6fb716bc98f67529692800890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9886678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4499104940e0fa941c243d4a5ebb14680ddb669eebe68c76d43135bd0394b192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:17 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:52:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:52:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee372f90f7ef23f31fc76a4466019b404611cba2e1f4a82317e3fd174737c5fb`  
		Last Modified: Mon, 09 Mar 2026 18:52:22 GMT  
		Size: 6.7 MB (6662076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782574ae05373a4c7aaad081baa71f5f14cf04ab763e551520f07b608e844a82`  
		Last Modified: Mon, 09 Mar 2026 18:52:21 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c96324057f5c8d157acda69af914ce19f59de7fa965cb6a4bd691a7f1944555`  
		Last Modified: Mon, 09 Mar 2026 18:52:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:68aabd30ac7da2e7ac9eb6308d6e8a08fc09f6546ad0b24bb051def4af9a05fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f226fba3a2d5c6701fb29ee41c8435592e958865ac681fef6db5deba3ef79543`

```dockerfile
```

-	Layers:
	-	`sha256:3c8546801f2a3a4def6a755cd20e911d8598e65a56558b18813ec1de41e5afc1`  
		Last Modified: Mon, 09 Mar 2026 18:52:21 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:02c7f3b39c5cf3d10caccf5f4524373b93abcac692a33d228cf302fa6c3e82cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaa889f217eda6bc3309fd495ff0288ce78da3d3ca2c4110eac79a412ee96ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e6cca90248248a19d6d2ccbda3eedcdc3b71cbce2e53cb7edce4fafc56089`  
		Last Modified: Mon, 09 Mar 2026 18:36:07 GMT  
		Size: 6.4 MB (6363581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb2bc8a416a183950dca40651c0946d74f0e709b5bd578402b15551d45ec577`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707706a624b809d68d0e8d5846e94c45235f68726ac9f1aad02f5fe512636105`  
		Last Modified: Mon, 09 Mar 2026 18:36:07 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4dc38af4737ae8a1ab3be0c1706cc5df71fce8247972b4afb73ea53226fc9460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1423c74c81db8555f3a363238d4224e27f3a35b22fc62ea2a1365379b3daef`

```dockerfile
```

-	Layers:
	-	`sha256:694d4f8ef199f5e518d91811709e4b1ebc441456a31c818c796e9aadd07211b0`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:03b91592b1efcb3ee215fd383f2da970e3d88f0d1df52ef21d37a0da016f3b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10149354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b2fe7d41f7d3e0aba8c363069d8154accefea84ec87345502ef8301b4f9fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:58 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 20:25:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 20:25:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6594a8ecb02ec426fd3d42bec247ff6ab3a0bc3947c86564ec3609674c982f00`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 6.4 MB (6414085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fab72cd5a3b23289d841e473149364f0766e0bc1ecb4c8e6b74cab2498aaa78`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2214f65a5029f801e92d99696aee8bcfefa538aced9a8e606f6d33157cf1434`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:24c91e19cdd6d603efe2e4ed798d998aac6225413965fafda5e6e7fb4d16b839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7525a6a7ff38f760c7ec03b459526de6d8c475a962479ef93a664a602718ced`

```dockerfile
```

-	Layers:
	-	`sha256:8a7eb5ea3dff9874ea8eda0f28e1272e2fc2e385768c5b9ae9fc26223da280e3`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:4f54d07ef5c090f9f6e9ccddbc816c25cb62f6bb86e035a89fd1b14a49f0a810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10441643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218aff781746e1c75173452b5771a042505bcf51b7c6e7835fcfb5a43d9ad97c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:31 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 19:01:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 19:01:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:32 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:32 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3e2be78bf35c5825460e3cd9df26e7d3d2a9c57d0165366cc3b0155f3401f`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 6.8 MB (6790239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4087688812b19faf72a90974cd2fbd774f27e3b601aa034f4e68bac91f750b`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1089a9c557806062528f3512e2220ab0ad9cd62d50421c79e2b53e695b406`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:949589dacc2f0ecbb6e48ced261b41d95193c11e6ffb71a8f5ed931d6e5a878e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed85ee3d490bc28df09944454d3a94b21d7ff3df30ee572c5572930e5f2c6a8`

```dockerfile
```

-	Layers:
	-	`sha256:5dfffe42ed310fa1683f5b64866a1bce41e0e25dfdf36b5adf97379ded5499f5`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:58ebbf8180181c2d581488c720ec9bd5fd7455916d0ed7cc64df305a618adca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:b0c37fffebabe483f975db48af95c240c8d108c1dd1dc3862e88f0147f369819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10752953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d25602f9385026b3db3fb35d2eedf14d53ef200ee624d741f5acc1f6b6bf69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:41 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:34:41 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:34:41 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:41 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f00b7901d8dee0560a03078f612f2cb3413aeddef2accf6482b430a82879db`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 6.9 MB (6947107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af7185d097383bbf95a4d1d24f5faf9e2f2cb92b4e5059268de4b7c9f0e3e5`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e325fad7fcbdb59dc485bf150a3a7453802f095e111db6d81c320dd55d656dd`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a6501e31f32a154a85a64c2f212c464f81b702cee6d27e15fef26fb8f6544750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee9915f808e75fc71c73d5f98392a42bf85bdef9a436b6b6d7227946f8b2b8d`

```dockerfile
```

-	Layers:
	-	`sha256:0f6408ec8cf247b2de3f55f1ec74aaa58cbfa4fc89316cd9670e23a999700d77`  
		Last Modified: Mon, 09 Mar 2026 18:34:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:771bf4346560cfb3d930014ac3fbf5186aa662ecfc9645f98d4c57e018a59cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10178135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e374b2e6ac4595c12866b39853a121ce0072c732a6d3999c924e5ed712d2f17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:42 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:48:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:48:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6475bea2ea18d0283bcf65bee880a4f50ab166ed503ead4d039037781e0e726`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 6.7 MB (6672120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966e5bc2ba77ffdb050c8a28a0b18e6c0662b211602eb7a7895ff3846c8ed549`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c866a98f69ad961fc3f0ed0d66124b9c020dd64bcd898032a6b54620fc4db3f`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:002d5873835f745f6e8179fd77bb0341743724bc64c06a314767f5932d836311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4562dc25f9df3852ff268d05036f470baaa595febdb93a0b81815a8c1aa94a`

```dockerfile
```

-	Layers:
	-	`sha256:b0991311b20547169d644dbeec09e5adb2d667f9304d10c3efbcdc7e0b188db3`  
		Last Modified: Mon, 09 Mar 2026 18:48:46 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:9c1eb92bafe472b4b8b57140a21b74bbe7518eb6fb716bc98f67529692800890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9886678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4499104940e0fa941c243d4a5ebb14680ddb669eebe68c76d43135bd0394b192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:17 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:52:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:52:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:17 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:17 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee372f90f7ef23f31fc76a4466019b404611cba2e1f4a82317e3fd174737c5fb`  
		Last Modified: Mon, 09 Mar 2026 18:52:22 GMT  
		Size: 6.7 MB (6662076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782574ae05373a4c7aaad081baa71f5f14cf04ab763e551520f07b608e844a82`  
		Last Modified: Mon, 09 Mar 2026 18:52:21 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c96324057f5c8d157acda69af914ce19f59de7fa965cb6a4bd691a7f1944555`  
		Last Modified: Mon, 09 Mar 2026 18:52:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:68aabd30ac7da2e7ac9eb6308d6e8a08fc09f6546ad0b24bb051def4af9a05fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f226fba3a2d5c6701fb29ee41c8435592e958865ac681fef6db5deba3ef79543`

```dockerfile
```

-	Layers:
	-	`sha256:3c8546801f2a3a4def6a755cd20e911d8598e65a56558b18813ec1de41e5afc1`  
		Last Modified: Mon, 09 Mar 2026 18:52:21 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:02c7f3b39c5cf3d10caccf5f4524373b93abcac692a33d228cf302fa6c3e82cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaa889f217eda6bc3309fd495ff0288ce78da3d3ca2c4110eac79a412ee96ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e6cca90248248a19d6d2ccbda3eedcdc3b71cbce2e53cb7edce4fafc56089`  
		Last Modified: Mon, 09 Mar 2026 18:36:07 GMT  
		Size: 6.4 MB (6363581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb2bc8a416a183950dca40651c0946d74f0e709b5bd578402b15551d45ec577`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707706a624b809d68d0e8d5846e94c45235f68726ac9f1aad02f5fe512636105`  
		Last Modified: Mon, 09 Mar 2026 18:36:07 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4dc38af4737ae8a1ab3be0c1706cc5df71fce8247972b4afb73ea53226fc9460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1423c74c81db8555f3a363238d4224e27f3a35b22fc62ea2a1365379b3daef`

```dockerfile
```

-	Layers:
	-	`sha256:694d4f8ef199f5e518d91811709e4b1ebc441456a31c818c796e9aadd07211b0`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:03b91592b1efcb3ee215fd383f2da970e3d88f0d1df52ef21d37a0da016f3b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10149354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b2fe7d41f7d3e0aba8c363069d8154accefea84ec87345502ef8301b4f9fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:58 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 20:25:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 20:25:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6594a8ecb02ec426fd3d42bec247ff6ab3a0bc3947c86564ec3609674c982f00`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 6.4 MB (6414085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fab72cd5a3b23289d841e473149364f0766e0bc1ecb4c8e6b74cab2498aaa78`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2214f65a5029f801e92d99696aee8bcfefa538aced9a8e606f6d33157cf1434`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:24c91e19cdd6d603efe2e4ed798d998aac6225413965fafda5e6e7fb4d16b839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7525a6a7ff38f760c7ec03b459526de6d8c475a962479ef93a664a602718ced`

```dockerfile
```

-	Layers:
	-	`sha256:8a7eb5ea3dff9874ea8eda0f28e1272e2fc2e385768c5b9ae9fc26223da280e3`  
		Last Modified: Mon, 09 Mar 2026 20:26:06 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:4f54d07ef5c090f9f6e9ccddbc816c25cb62f6bb86e035a89fd1b14a49f0a810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10441643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218aff781746e1c75173452b5771a042505bcf51b7c6e7835fcfb5a43d9ad97c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:31 GMT
ENV NATS_SERVER=2.11.14
# Mon, 09 Mar 2026 19:01:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Mon, 09 Mar 2026 19:01:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b3a18f49acd75101b8d42671b11c2a4e671175cf90e52f1fe73c70ca02b6c8f9' ;;     armhf) natsArch='arm6'; sha256='db1ddf3f0cb7d0374d553b06da3a5f805e73633d34bb767099dd8ffd1775992b' ;;     armv7) natsArch='arm7'; sha256='a4ba6f0ee49d1ec270766d20d9003f9e9de2d91d8fdd3b04a1464c25a28a1798' ;;     x86_64) natsArch='amd64'; sha256='1e8843593565abc7e3280238a2648537805025d1cd66244bf884ac3b45a6e3a8' ;;     x86) natsArch='386'; sha256='50cc562791aa4bcbeaf72c4bf6b2a42dc67da68aede7a3c495c5b65370b7bff7' ;;     s390x) natsArch='s390x'; sha256='6d5efb93403b638522b1516b425497c1220df112f6b2bd4c297772e0fcf2c2c2' ;;     ppc64le) natsArch='ppc64le'; sha256='b8c08c856990f5e1d038dcb91a652ae68815c227654493bca714be8bf92c622a' ;;     loong64) natsArch='loong64'; sha256='630f7b7001155df394df403629be602067c1746703a54a4378e7bf57dd190990' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:32 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:32 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3e2be78bf35c5825460e3cd9df26e7d3d2a9c57d0165366cc3b0155f3401f`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 6.8 MB (6790239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4087688812b19faf72a90974cd2fbd774f27e3b601aa034f4e68bac91f750b`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1089a9c557806062528f3512e2220ab0ad9cd62d50421c79e2b53e695b406`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:949589dacc2f0ecbb6e48ced261b41d95193c11e6ffb71a8f5ed931d6e5a878e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed85ee3d490bc28df09944454d3a94b21d7ff3df30ee572c5572930e5f2c6a8`

```dockerfile
```

-	Layers:
	-	`sha256:5dfffe42ed310fa1683f5b64866a1bce41e0e25dfdf36b5adf97379ded5499f5`  
		Last Modified: Mon, 09 Mar 2026 19:01:39 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:ab70df1e97d372a3f059918fba241a1dbe0cb3604044584d44c5f2b804c6d94c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:49c32c87bec99746a8b30c2f1b4f75b4f523e229449735b31fb0a862955b5d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6489015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84937fc8d4b2ea427a9288296a8e1550d90adfd678004ec184ff891d05194455`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:44 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:01b31e3d8e4b92d54d5280ce1923156df749289333050774805f4ee3d6604985`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.5 MB (6488506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7736bcae51bba47854c82d0063b92a3a61826af7e6dadba0def0eab42726b14`  
		Last Modified: Mon, 09 Mar 2026 19:12:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9c07ccf3d70484b44c3828d9555784bf274d430d92ede4d1796c21d0be998585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1c288b1e85e54be02734d0b651cd0b3d32b72627aae2f30ead31f99652e273`

```dockerfile
```

-	Layers:
	-	`sha256:5af6cc00e9a512cc3c76556ae551449e273f48c36c6e44964d7c72d8f0cabfea`  
		Last Modified: Mon, 09 Mar 2026 19:12:49 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:925f78234d1ac10f9228b170aae2705acc585485e468496eaa76eb6d4eeeac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667802c2ce4b89d852e3b146d8806596bb57115022ff32978e8232c29f668a4a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:32 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:32 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:32 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a7277d8d113dec8b315d7940efa55fb3c3a6e91626be07e09fabffdb888af61`  
		Last Modified: Mon, 09 Mar 2026 16:09:45 GMT  
		Size: 6.2 MB (6212623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd98f25d5ef9e8bf9b99604eaa363092b8f7500f9c127cb6e7b0cd93a64f062`  
		Last Modified: Mon, 09 Mar 2026 21:49:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2f0e8526bcb8e60bfd9c305adc9a3a520763f0c9cab98b74b6b93c30f0e3749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6eb54dc8f395b0cd2162dbffc902620efc9011f71a7f9acce9ba1ee40516349`

```dockerfile
```

-	Layers:
	-	`sha256:acadba40a6f29e93baf61c470cc428238af6e70b7a768143a5bfa122463d7698`  
		Last Modified: Mon, 09 Mar 2026 21:49:36 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8168117cee667bc4d9f9e684c1f2324c54fcb6c873ee8e6253acf0e904550135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ebc16f64dc50aed83704d38077d99f7c19b9da02a0cfa81260db2f81009ce4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7960b0843dc07a38a4f69f7d3ae72c7e4c393207293594028277c1c6fa469cc5`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.2 MB (6205764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a5c7f1d5f5c1920740cf15921f65d41e3220fc251e3511dfc6ae3e9531d737`  
		Last Modified: Mon, 09 Mar 2026 21:53:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:127f56764c95373649dfb4b00ce4e03a80a82af31ae70b87e489b2fb1c70ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c11a7cb933860a45f2843890d2e4b8349abedea08888d133122e68f037f8e30`

```dockerfile
```

-	Layers:
	-	`sha256:56f907fa91fdd38de99f07a9e06a9c6f02ca279b0dc5842384a8adca4d5fa4a8`  
		Last Modified: Mon, 09 Mar 2026 21:53:18 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f153f55bb9f5e7c1eea5420d42a96c289a0f00006c2dd87aca1bbbfa130b14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5909462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a671f51ee515bfccdbbda9704f971ce62d649d92ed07a09c52ea3e585338668`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3e32192681ac27bc253f38f45ca0d5b2ad36ba165acc96342765c068290a3796`  
		Last Modified: Mon, 09 Mar 2026 16:09:45 GMT  
		Size: 5.9 MB (5908952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261d013df878cf62dac4f23852a22ce188b63518350e086e2d9caee1e9aef7`  
		Last Modified: Mon, 09 Mar 2026 19:12:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:35e1227b1a8949f792c6fa82a6ff1d0c3ee628f5b851524df86d4361f04c1684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44ab2b9d0255e052be33a525127dff84a7af1da36ccd121c82f7c61a7270cf1`

```dockerfile
```

-	Layers:
	-	`sha256:b5e81d8bd95602e874a18e803af3066a1a40ab909c35b9889aa58ebc23002ef3`  
		Last Modified: Mon, 09 Mar 2026 19:12:27 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:dd35dbfa99c5fcec2325bc24647f409ac503e74f8e37872006b7ae01540ec802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a180d825c868c7c0dc0e087a116313a4844d95f6474e36d0c1b42ec66c1b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7db64218ee876daffe3f2d1117157a1265b22c9cf8500c591c02d8cf2157b901`  
		Last Modified: Mon, 09 Mar 2026 16:09:42 GMT  
		Size: 6.0 MB (5958115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a656cf595bc0cf59dda8f8a382852db660e89b23335bdc816f62ba7917cfe65`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:dd21301252bd4aa3ff3fc7021490740066e3017782a31ae4134c26884fec95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56459d873e6b8b8442c8994c72f4a757c4a21b973448ba17883850c1acc46e3`

```dockerfile
```

-	Layers:
	-	`sha256:a1e5736bab434f9ed5f26403ff3ebf6d0d8f1eb29a91344a829ac31cb6ea136f`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:17c0134c00f91e8f138a33efbc730597da0f1520b705428d2d35ef9ec55e885a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a714c69afcbf633ec367b366c5ffaea6a256b35510b878c49731e45c0daad6ae`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:16 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84d2ac1d4fe9a738e55809ec9f070c1f06c8941abb334c06b7269033719fa09b`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.3 MB (6329356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ca2e0276ecac592aba65dfafef7bb374ad3533206f35178cd658c0a6801d67`  
		Last Modified: Mon, 09 Mar 2026 19:11:24 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:18aad3846a8d8b263b848d12942c0e669493d6e3d5e171fc8b5edfc4a731cf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e7663af8889626ff642c6b24a89ec101e0afc0f8fb225d7a6cc33df5b4a91`

```dockerfile
```

-	Layers:
	-	`sha256:6b7de3173d9fdb8824cded52df758f8a406c8168c7b839e77e641ad60b73d732`  
		Last Modified: Mon, 09 Mar 2026 19:11:24 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:4fd5d3fb56200d0933e72e4f9872154a952d7af594b2353f837cc29a74311fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:cb62597c55ed0e4879a76d7954dcfe510e9ae2c407ef07d7f6162cb1e546ea6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133324190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb885af05de0690a25ffe5ed510dd7780920301fa4f8409a563709978406036`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:37:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:38:01 GMT
RUN cmd /S /C #(nop) COPY file:690296852f806393ad867a961bb2117053cdde9e33cb62cfc133cf2222b12dde in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:38:02 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:38:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:38:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:38:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe9bc4bba5a63f8196fe0b5ef4ad39026bb53e1400380d906e8ed27489d49a`  
		Last Modified: Tue, 10 Mar 2026 22:38:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3dff46f73915f0c1b07ff70feb495b9fc958f0feb4e98841dd5893831f63b6`  
		Last Modified: Tue, 10 Mar 2026 22:38:09 GMT  
		Size: 6.7 MB (6667782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cdf89affe03acb92a2a6462b75875142d25904087ee6ef04a352a05ac129d7`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2309fea759ab93e8e58a8eaf26bd7f55af17ac581cd812227437bded0e1088`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540a38924fe9c502f31944994dcba191d8e58b7ac043443f22fe21bc664fa0b3`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71528307feff7f868710b39b8b35d3859481c3c704074a90356625664fdd9243`  
		Last Modified: Tue, 10 Mar 2026 22:38:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4fd5d3fb56200d0933e72e4f9872154a952d7af594b2353f837cc29a74311fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:cb62597c55ed0e4879a76d7954dcfe510e9ae2c407ef07d7f6162cb1e546ea6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133324190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb885af05de0690a25ffe5ed510dd7780920301fa4f8409a563709978406036`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:37:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:38:01 GMT
RUN cmd /S /C #(nop) COPY file:690296852f806393ad867a961bb2117053cdde9e33cb62cfc133cf2222b12dde in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:38:02 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:38:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:38:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:38:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe9bc4bba5a63f8196fe0b5ef4ad39026bb53e1400380d906e8ed27489d49a`  
		Last Modified: Tue, 10 Mar 2026 22:38:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3dff46f73915f0c1b07ff70feb495b9fc958f0feb4e98841dd5893831f63b6`  
		Last Modified: Tue, 10 Mar 2026 22:38:09 GMT  
		Size: 6.7 MB (6667782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cdf89affe03acb92a2a6462b75875142d25904087ee6ef04a352a05ac129d7`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2309fea759ab93e8e58a8eaf26bd7f55af17ac581cd812227437bded0e1088`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540a38924fe9c502f31944994dcba191d8e58b7ac043443f22fe21bc664fa0b3`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71528307feff7f868710b39b8b35d3859481c3c704074a90356625664fdd9243`  
		Last Modified: Tue, 10 Mar 2026 22:38:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:ab70df1e97d372a3f059918fba241a1dbe0cb3604044584d44c5f2b804c6d94c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:49c32c87bec99746a8b30c2f1b4f75b4f523e229449735b31fb0a862955b5d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6489015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84937fc8d4b2ea427a9288296a8e1550d90adfd678004ec184ff891d05194455`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:44 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:01b31e3d8e4b92d54d5280ce1923156df749289333050774805f4ee3d6604985`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.5 MB (6488506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7736bcae51bba47854c82d0063b92a3a61826af7e6dadba0def0eab42726b14`  
		Last Modified: Mon, 09 Mar 2026 19:12:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9c07ccf3d70484b44c3828d9555784bf274d430d92ede4d1796c21d0be998585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1c288b1e85e54be02734d0b651cd0b3d32b72627aae2f30ead31f99652e273`

```dockerfile
```

-	Layers:
	-	`sha256:5af6cc00e9a512cc3c76556ae551449e273f48c36c6e44964d7c72d8f0cabfea`  
		Last Modified: Mon, 09 Mar 2026 19:12:49 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:925f78234d1ac10f9228b170aae2705acc585485e468496eaa76eb6d4eeeac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667802c2ce4b89d852e3b146d8806596bb57115022ff32978e8232c29f668a4a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:32 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:32 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:32 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a7277d8d113dec8b315d7940efa55fb3c3a6e91626be07e09fabffdb888af61`  
		Last Modified: Mon, 09 Mar 2026 16:09:45 GMT  
		Size: 6.2 MB (6212623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd98f25d5ef9e8bf9b99604eaa363092b8f7500f9c127cb6e7b0cd93a64f062`  
		Last Modified: Mon, 09 Mar 2026 21:49:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2f0e8526bcb8e60bfd9c305adc9a3a520763f0c9cab98b74b6b93c30f0e3749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6eb54dc8f395b0cd2162dbffc902620efc9011f71a7f9acce9ba1ee40516349`

```dockerfile
```

-	Layers:
	-	`sha256:acadba40a6f29e93baf61c470cc428238af6e70b7a768143a5bfa122463d7698`  
		Last Modified: Mon, 09 Mar 2026 21:49:36 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:8168117cee667bc4d9f9e684c1f2324c54fcb6c873ee8e6253acf0e904550135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ebc16f64dc50aed83704d38077d99f7c19b9da02a0cfa81260db2f81009ce4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7960b0843dc07a38a4f69f7d3ae72c7e4c393207293594028277c1c6fa469cc5`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.2 MB (6205764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a5c7f1d5f5c1920740cf15921f65d41e3220fc251e3511dfc6ae3e9531d737`  
		Last Modified: Mon, 09 Mar 2026 21:53:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:127f56764c95373649dfb4b00ce4e03a80a82af31ae70b87e489b2fb1c70ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c11a7cb933860a45f2843890d2e4b8349abedea08888d133122e68f037f8e30`

```dockerfile
```

-	Layers:
	-	`sha256:56f907fa91fdd38de99f07a9e06a9c6f02ca279b0dc5842384a8adca4d5fa4a8`  
		Last Modified: Mon, 09 Mar 2026 21:53:18 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f153f55bb9f5e7c1eea5420d42a96c289a0f00006c2dd87aca1bbbfa130b14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5909462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a671f51ee515bfccdbbda9704f971ce62d649d92ed07a09c52ea3e585338668`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3e32192681ac27bc253f38f45ca0d5b2ad36ba165acc96342765c068290a3796`  
		Last Modified: Mon, 09 Mar 2026 16:09:45 GMT  
		Size: 5.9 MB (5908952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261d013df878cf62dac4f23852a22ce188b63518350e086e2d9caee1e9aef7`  
		Last Modified: Mon, 09 Mar 2026 19:12:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:35e1227b1a8949f792c6fa82a6ff1d0c3ee628f5b851524df86d4361f04c1684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44ab2b9d0255e052be33a525127dff84a7af1da36ccd121c82f7c61a7270cf1`

```dockerfile
```

-	Layers:
	-	`sha256:b5e81d8bd95602e874a18e803af3066a1a40ab909c35b9889aa58ebc23002ef3`  
		Last Modified: Mon, 09 Mar 2026 19:12:27 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:dd35dbfa99c5fcec2325bc24647f409ac503e74f8e37872006b7ae01540ec802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a180d825c868c7c0dc0e087a116313a4844d95f6474e36d0c1b42ec66c1b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7db64218ee876daffe3f2d1117157a1265b22c9cf8500c591c02d8cf2157b901`  
		Last Modified: Mon, 09 Mar 2026 16:09:42 GMT  
		Size: 6.0 MB (5958115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a656cf595bc0cf59dda8f8a382852db660e89b23335bdc816f62ba7917cfe65`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:dd21301252bd4aa3ff3fc7021490740066e3017782a31ae4134c26884fec95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56459d873e6b8b8442c8994c72f4a757c4a21b973448ba17883850c1acc46e3`

```dockerfile
```

-	Layers:
	-	`sha256:a1e5736bab434f9ed5f26403ff3ebf6d0d8f1eb29a91344a829ac31cb6ea136f`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:17c0134c00f91e8f138a33efbc730597da0f1520b705428d2d35ef9ec55e885a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a714c69afcbf633ec367b366c5ffaea6a256b35510b878c49731e45c0daad6ae`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:16 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84d2ac1d4fe9a738e55809ec9f070c1f06c8941abb334c06b7269033719fa09b`  
		Last Modified: Mon, 09 Mar 2026 16:09:46 GMT  
		Size: 6.3 MB (6329356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ca2e0276ecac592aba65dfafef7bb374ad3533206f35178cd658c0a6801d67`  
		Last Modified: Mon, 09 Mar 2026 19:11:24 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:18aad3846a8d8b263b848d12942c0e669493d6e3d5e171fc8b5edfc4a731cf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e7663af8889626ff642c6b24a89ec101e0afc0f8fb225d7a6cc33df5b4a91`

```dockerfile
```

-	Layers:
	-	`sha256:6b7de3173d9fdb8824cded52df758f8a406c8168c7b839e77e641ad60b73d732`  
		Last Modified: Mon, 09 Mar 2026 19:11:24 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:80c367a9ca19ebd7046d9d4fdaaf8fa201cc3a2c619f50bbbc535fb8cba8ffee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:70bdb60a545c0a071e6d97308cbe4b0593f5f49cea4e965d82a2bd573a6c3abe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989786885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bfb0cfe52ea0255e45bd161a7cf50853894e81add473d3fd2d0fef5d6d65c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 22:02:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:02:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:02:29 GMT
ENV NATS_SERVER=2.11.14
# Tue, 10 Mar 2026 22:02:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Tue, 10 Mar 2026 22:02:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.14/nats-server-v2.11.14-windows-amd64.zip
# Tue, 10 Mar 2026 22:02:31 GMT
ENV NATS_SERVER_SHASUM=ca42a42de5af435245ff3932f11aad9d4b968d2c1c7d6f4644a46d2a7f8ef6d1
# Tue, 10 Mar 2026 22:02:37 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 22:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 22:02:57 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:02:57 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:02:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e189237dfb744c7f2397f90bd4ac365c8236ac38f9f0a87efe03abcca842bf09`  
		Last Modified: Tue, 10 Mar 2026 22:03:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d1e98face2c1e1bb32f8e9ba3c2f35448563fd9dd6e04195a4c78b5ab62601`  
		Last Modified: Tue, 10 Mar 2026 22:03:07 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cc1aae40f69238b5fc06a60a5eca7798f9ba720a7c7ba8f1b88b77d912079b`  
		Last Modified: Tue, 10 Mar 2026 22:03:07 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9188999589b8b3cd1fad7fab181f7800ca02285e6769bb8737b150786b586764`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42ac2c8f3bfaeee58e0cb03804264d9108fa8bb778677f8c3be89c289a3de5a`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bc47db603d5697bb3c5f0fe666585810908faf94fe789404beb3ed43f280f8`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f98aed2bec07272837f5ba73f4c5d695f56e1ab75f799dfc3a8c653904ec793`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 479.0 KB (479022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92636205ffad066e5e070a4be90ce5ef772d77868fed5a4a7423fdfd9dac0fad`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 7.0 MB (7012764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b43b3b1d469ba0d1a2642226bb991c99e19ebf4619ff8c6e10b8ad639a7a436`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf277acef2d4d36f6d0adf257af0d3b52f38faaf161308a92b8d25f1fae343e5`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529a6dd670c5545cfc90efdf497a231b04f4258b66cd0bc15ec231b78df4eeb9`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f992cc05e85bd9f03ac3710d86aea850d9c11aeca6a8ffcfec80234a7c5b5ae3`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:80c367a9ca19ebd7046d9d4fdaaf8fa201cc3a2c619f50bbbc535fb8cba8ffee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:70bdb60a545c0a071e6d97308cbe4b0593f5f49cea4e965d82a2bd573a6c3abe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989786885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bfb0cfe52ea0255e45bd161a7cf50853894e81add473d3fd2d0fef5d6d65c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 22:02:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:02:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:02:29 GMT
ENV NATS_SERVER=2.11.14
# Tue, 10 Mar 2026 22:02:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.14
# Tue, 10 Mar 2026 22:02:30 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.14/nats-server-v2.11.14-windows-amd64.zip
# Tue, 10 Mar 2026 22:02:31 GMT
ENV NATS_SERVER_SHASUM=ca42a42de5af435245ff3932f11aad9d4b968d2c1c7d6f4644a46d2a7f8ef6d1
# Tue, 10 Mar 2026 22:02:37 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 22:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 22:02:57 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:02:57 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:02:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e189237dfb744c7f2397f90bd4ac365c8236ac38f9f0a87efe03abcca842bf09`  
		Last Modified: Tue, 10 Mar 2026 22:03:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d1e98face2c1e1bb32f8e9ba3c2f35448563fd9dd6e04195a4c78b5ab62601`  
		Last Modified: Tue, 10 Mar 2026 22:03:07 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cc1aae40f69238b5fc06a60a5eca7798f9ba720a7c7ba8f1b88b77d912079b`  
		Last Modified: Tue, 10 Mar 2026 22:03:07 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9188999589b8b3cd1fad7fab181f7800ca02285e6769bb8737b150786b586764`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42ac2c8f3bfaeee58e0cb03804264d9108fa8bb778677f8c3be89c289a3de5a`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bc47db603d5697bb3c5f0fe666585810908faf94fe789404beb3ed43f280f8`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f98aed2bec07272837f5ba73f4c5d695f56e1ab75f799dfc3a8c653904ec793`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 479.0 KB (479022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92636205ffad066e5e070a4be90ce5ef772d77868fed5a4a7423fdfd9dac0fad`  
		Last Modified: Tue, 10 Mar 2026 22:03:05 GMT  
		Size: 7.0 MB (7012764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b43b3b1d469ba0d1a2642226bb991c99e19ebf4619ff8c6e10b8ad639a7a436`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf277acef2d4d36f6d0adf257af0d3b52f38faaf161308a92b8d25f1fae343e5`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529a6dd670c5545cfc90efdf497a231b04f4258b66cd0bc15ec231b78df4eeb9`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f992cc05e85bd9f03ac3710d86aea850d9c11aeca6a8ffcfec80234a7c5b5ae3`  
		Last Modified: Tue, 10 Mar 2026 22:03:03 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.15`

**does not exist** (yet?)

## `nats:2.11.15-alpine`

**does not exist** (yet?)

## `nats:2.11.15-alpine3.22`

**does not exist** (yet?)

## `nats:2.11.15-linux`

**does not exist** (yet?)

## `nats:2.11.15-nanoserver`

**does not exist** (yet?)

## `nats:2.11.15-nanoserver-ltsc2022`

**does not exist** (yet?)

## `nats:2.11.15-scratch`

**does not exist** (yet?)

## `nats:2.11.15-windowsservercore`

**does not exist** (yet?)

## `nats:2.11.15-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `nats:2.12`

```console
$ docker pull nats@sha256:7971c76fcd4057c090faf5bc7673199ffe0ae586704518e9a469f156155b4e47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:c1379a8588df47244a4789ede85e8ae7490bd37006bde837e4d6fb6f559cb0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:f55092a58ef4b6883fd9b9e67c8741139c3701acff2d7e57930abbb54d2d4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10886061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81529466020c291e5ad80f56987ed653d491e1b9476ccbdeaf67b72affa3c278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8887a98e8249b73b0777bfbc8c0a30b02d3c21e3c39a9d768c5871b5585777`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 7.1 MB (7080215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dead58ebc17268f1b2f4cec215f560e3a07cc610d28eeff77d5f1c5d8e2517`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b4cd24f67b5d5afe059593810655b6887ba69dbdb160f71907e3daca8a8dc`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:685e730f881ec97c5e115e96bfe8066a26a611e53bcbfa4f0e69d4b4a174b46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb00ece4ca5cf51cc4d452e9249450fed5b54cfe2a9112947dca28d2ea8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3ba67a28104834d1d93b1e7e33ff17be9085f62d4b1100860816af7c9e0de`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c7bf3f984b3b64f0c1f9f4674a8f76c32e17a58c3a69291ad03b749fb8275ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52985b6ab22ea9e18f31378c7d723405b36c8533ab7e35049e80e606ec5042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148f12e063d142770b6e05b9f9c2ab014ab5763dff5f40cf43b4d8741dea20e0`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 6.8 MB (6797772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb32797a1c1b66b3d5d82193923eb3b39bbd560af58c01e71d7f46127eda32c`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c38be02f7f6968455354dfe4a4a05e5f20fbcdad07b63a3add2b522b3fc163`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7f5278fc819e312da44d7f8c6548fbd4f008b7047b81aaec0c88e1b6e7bf80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf1a9035fbf11bd94daf97ff6446b8c962f779e52915fdb47f723375a90161`

```dockerfile
```

-	Layers:
	-	`sha256:d069f32f6e0103cf7962bc3e50c1be2b0953ab9edcfb7db9f63defe80ce6c7b2`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de66d6fac8ce8ebef0e1032f68c75720b2d9fe3a040132c69bce4613ae04a5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10016287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb89708d609d7d7c02e11f18dbd6f2ebbd095aee4402d8d2d9a9c4ca7917e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627631ba1918c54c7a3365b569389ba221a3fcbd467f2f68c02834aa91cc94f`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 6.8 MB (6791688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909a283e1b0f458613bac969dccdc3e622f3167995890a9b73344d1afe42e0c`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc1d6c83015eb80bc6e00a18fd3fe4b50483b56a1b8d381db8551986ad949e`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a89cb4125128c4481995506bc126626436c2a4398b4d1ca640b05c513c9c3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576436877db30f3cde211a66a4c4013292cae5b6f4cdcba857a0f440e84397a8`

```dockerfile
```

-	Layers:
	-	`sha256:c681f3aa2919334b313a7f825221815da8a74b0c5717aece45a141747c4666a4`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ce72c5047aac010d13d69e087e2ef792ba483b581d3fe131a06f24f4bcd64499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10629509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78db93426f4ce81493b1740958536016471acce7c2469d30642d1ce5e2505028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825bb7632b2910036c4e99446261eaccf38a5407182667a9a5544165b29a3a66`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 6.5 MB (6489020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a075238f2783d207491918f497c4935823239fef8402991a1501e453f6dba`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e51ee93c455d52b0a680fe79d12a069061e5d506026beeda5e511a4b3221a49`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6803835c0dc24ce636ea74af20236401d626a7086072c838f1bdc957a100b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389309d70c5e974ba909c72462ccaecc37686be93ec78f5b3f4ec005cb0760b`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a9525024c9f083b6bf1027d0683e9da385aa15944aa3dd296418810f297b6`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:ea21e6eb9baed3f48d70928e28581f139ea88123ae96c10ab7fd753b196f711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6294e924a35b3ba351e1a9cb918458e4656b4bf790282e9b5b571ef60785615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:50 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f47dcf083e6405dbb62b78c40e89eddfa579782e18796398d04ac483723b67`  
		Last Modified: Mon, 09 Mar 2026 20:26:00 GMT  
		Size: 6.5 MB (6538200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cff225f6b222724626788da2eb98a26c2385e0464e86d59d843ae8cd9131b`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264d913d41a7e5acf68f5c7336a947d1c985b3beb40308165f5e1529c5e7e1`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c395e1e7cdcf166da464ce9b176a78f41cc1e379d12029384d18535e7510dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd1e702aa11e4a3b35ba6f6d3a008217124ef4d19d93d23e12767750a22642b`

```dockerfile
```

-	Layers:
	-	`sha256:1eed2a8cf66e0339f0d26be0f99591e27aa134d22ad734dce841c59737673453`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:922a66519e1e1d9166fcdf6ffc4ee018befd6cde9b8b53d7e614d2e41ed770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a50c0d0127f61de22b52cfc3acbf5c208e15f76b7a6e18a51e075465786d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:21 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a6cdb957401649789e5b4f2cbe88f55a7b8e0a8bd0609c92d9eef2c3a417e`  
		Last Modified: Mon, 09 Mar 2026 19:01:30 GMT  
		Size: 6.9 MB (6920512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7111270df9c5fff857ec52c3ba39df86a8800642c13f0d00bd04a1712b9d4e0`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919a6d79781833003c5f530b73820bdd56e515c4670f1a782d6f68bd6cbaf8d`  
		Last Modified: Mon, 09 Mar 2026 19:01:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dd1073397e51e35ad7dd3e192c8a292dede602bcea951e4d02a8e2acc25cc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f173e09372d1c0d616aa2b5e814f124a00b622196f5122bbe8ceb997b7f93d`

```dockerfile
```

-	Layers:
	-	`sha256:f149e96bc2411d24ddb1f3bd40351a3b5649c09c2f17f7db57ca653a6e4731ee`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:c1379a8588df47244a4789ede85e8ae7490bd37006bde837e4d6fb6f559cb0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:f55092a58ef4b6883fd9b9e67c8741139c3701acff2d7e57930abbb54d2d4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10886061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81529466020c291e5ad80f56987ed653d491e1b9476ccbdeaf67b72affa3c278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8887a98e8249b73b0777bfbc8c0a30b02d3c21e3c39a9d768c5871b5585777`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 7.1 MB (7080215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dead58ebc17268f1b2f4cec215f560e3a07cc610d28eeff77d5f1c5d8e2517`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b4cd24f67b5d5afe059593810655b6887ba69dbdb160f71907e3daca8a8dc`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:685e730f881ec97c5e115e96bfe8066a26a611e53bcbfa4f0e69d4b4a174b46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb00ece4ca5cf51cc4d452e9249450fed5b54cfe2a9112947dca28d2ea8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3ba67a28104834d1d93b1e7e33ff17be9085f62d4b1100860816af7c9e0de`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c7bf3f984b3b64f0c1f9f4674a8f76c32e17a58c3a69291ad03b749fb8275ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52985b6ab22ea9e18f31378c7d723405b36c8533ab7e35049e80e606ec5042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148f12e063d142770b6e05b9f9c2ab014ab5763dff5f40cf43b4d8741dea20e0`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 6.8 MB (6797772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb32797a1c1b66b3d5d82193923eb3b39bbd560af58c01e71d7f46127eda32c`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c38be02f7f6968455354dfe4a4a05e5f20fbcdad07b63a3add2b522b3fc163`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7f5278fc819e312da44d7f8c6548fbd4f008b7047b81aaec0c88e1b6e7bf80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf1a9035fbf11bd94daf97ff6446b8c962f779e52915fdb47f723375a90161`

```dockerfile
```

-	Layers:
	-	`sha256:d069f32f6e0103cf7962bc3e50c1be2b0953ab9edcfb7db9f63defe80ce6c7b2`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:de66d6fac8ce8ebef0e1032f68c75720b2d9fe3a040132c69bce4613ae04a5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10016287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb89708d609d7d7c02e11f18dbd6f2ebbd095aee4402d8d2d9a9c4ca7917e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627631ba1918c54c7a3365b569389ba221a3fcbd467f2f68c02834aa91cc94f`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 6.8 MB (6791688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909a283e1b0f458613bac969dccdc3e622f3167995890a9b73344d1afe42e0c`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc1d6c83015eb80bc6e00a18fd3fe4b50483b56a1b8d381db8551986ad949e`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a89cb4125128c4481995506bc126626436c2a4398b4d1ca640b05c513c9c3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576436877db30f3cde211a66a4c4013292cae5b6f4cdcba857a0f440e84397a8`

```dockerfile
```

-	Layers:
	-	`sha256:c681f3aa2919334b313a7f825221815da8a74b0c5717aece45a141747c4666a4`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ce72c5047aac010d13d69e087e2ef792ba483b581d3fe131a06f24f4bcd64499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10629509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78db93426f4ce81493b1740958536016471acce7c2469d30642d1ce5e2505028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825bb7632b2910036c4e99446261eaccf38a5407182667a9a5544165b29a3a66`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 6.5 MB (6489020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a075238f2783d207491918f497c4935823239fef8402991a1501e453f6dba`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e51ee93c455d52b0a680fe79d12a069061e5d506026beeda5e511a4b3221a49`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6803835c0dc24ce636ea74af20236401d626a7086072c838f1bdc957a100b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389309d70c5e974ba909c72462ccaecc37686be93ec78f5b3f4ec005cb0760b`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a9525024c9f083b6bf1027d0683e9da385aa15944aa3dd296418810f297b6`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ea21e6eb9baed3f48d70928e28581f139ea88123ae96c10ab7fd753b196f711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6294e924a35b3ba351e1a9cb918458e4656b4bf790282e9b5b571ef60785615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:50 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f47dcf083e6405dbb62b78c40e89eddfa579782e18796398d04ac483723b67`  
		Last Modified: Mon, 09 Mar 2026 20:26:00 GMT  
		Size: 6.5 MB (6538200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cff225f6b222724626788da2eb98a26c2385e0464e86d59d843ae8cd9131b`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264d913d41a7e5acf68f5c7336a947d1c985b3beb40308165f5e1529c5e7e1`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c395e1e7cdcf166da464ce9b176a78f41cc1e379d12029384d18535e7510dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd1e702aa11e4a3b35ba6f6d3a008217124ef4d19d93d23e12767750a22642b`

```dockerfile
```

-	Layers:
	-	`sha256:1eed2a8cf66e0339f0d26be0f99591e27aa134d22ad734dce841c59737673453`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:922a66519e1e1d9166fcdf6ffc4ee018befd6cde9b8b53d7e614d2e41ed770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a50c0d0127f61de22b52cfc3acbf5c208e15f76b7a6e18a51e075465786d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:21 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a6cdb957401649789e5b4f2cbe88f55a7b8e0a8bd0609c92d9eef2c3a417e`  
		Last Modified: Mon, 09 Mar 2026 19:01:30 GMT  
		Size: 6.9 MB (6920512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7111270df9c5fff857ec52c3ba39df86a8800642c13f0d00bd04a1712b9d4e0`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919a6d79781833003c5f530b73820bdd56e515c4670f1a782d6f68bd6cbaf8d`  
		Last Modified: Mon, 09 Mar 2026 19:01:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:dd1073397e51e35ad7dd3e192c8a292dede602bcea951e4d02a8e2acc25cc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f173e09372d1c0d616aa2b5e814f124a00b622196f5122bbe8ceb997b7f93d`

```dockerfile
```

-	Layers:
	-	`sha256:f149e96bc2411d24ddb1f3bd40351a3b5649c09c2f17f7db57ca653a6e4731ee`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:4381ef3a8a655e7f0cca77861aa1b12801161df68c13147da4629b7bbdc1201e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-linux` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:4e65924c3379e91937053a1f79ed9a3a79bf8a7bb5b38caca931059d70656eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4e65924c3379e91937053a1f79ed9a3a79bf8a7bb5b38caca931059d70656eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:4381ef3a8a655e7f0cca77861aa1b12801161df68c13147da4629b7bbdc1201e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:9b0bc6e81344da3bd2751cf47d851dc71c28a7d7d30f7328b435c0d5083f3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:6ae257bf95b984fb32a4f6eeb280e11b127a5779eb61c1e4d2054e1163e39a06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989938833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf972a8f9ff2fce9f9ca75a08b35c399345e0347c096de0b4f53579fa7ad32d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:58:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 21:58:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 21:58:11 GMT
ENV NATS_SERVER=2.12.5
# Tue, 10 Mar 2026 21:58:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Tue, 10 Mar 2026 21:58:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.5/nats-server-v2.12.5-windows-amd64.zip
# Tue, 10 Mar 2026 21:58:14 GMT
ENV NATS_SERVER_SHASUM=29d6eca9ce085731bd63b32eeff7fae076938d31dd095acccfc70f2496d07ea7
# Tue, 10 Mar 2026 21:58:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 21:58:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 21:58:54 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 21:58:55 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 21:58:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 21:58:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04c32730da76e4f8c0992e8486404cface27cdbf86a7fe00437d3025590b7e`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02ad44b5ae354c11458cd62dee34cf93d9389058036580d4260d9551883ed0`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d2d6023a53e21e129bd012c45fed3f50dabc9d0bcea695e14ecdac1ad3f03`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0deaad7f12bcdc5138b621c8a8c2a35766f41f719b51f6add6f71d28a0842`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2a17f84ab038fcc41ab1c8aa33270d582ed981327779baf6d26e85c36b1f1c`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800dc056e1954416cde33967232d04ac013a4b298a04c3bb591bb6cda1a3696`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b556c3513211380357d8ba1d5774644200201d0a0973350c0b338eb7aecc6a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 484.7 KB (484712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e93160909732ff5d08e605284a33be5e2f51dd89a8ed9b5ad40bd5948a090`  
		Last Modified: Tue, 10 Mar 2026 21:59:04 GMT  
		Size: 7.2 MB (7159095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b56e0af4952401a1d938512f31f1e379baf7f63ec96da79f873f8cdf83c397`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d839d11021d15ecfbce6ae4d506186302258eabf46c50e87ce5c5b75ff02a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f70edc90f77cbdf7689415400d2da65bb2e9a269a97c7411d32ace56cba1ff`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5573ab3f95d8693954515f4dfd4b0a086da95b6c7456f05348de2e4c1eee1a2`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:9b0bc6e81344da3bd2751cf47d851dc71c28a7d7d30f7328b435c0d5083f3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:6ae257bf95b984fb32a4f6eeb280e11b127a5779eb61c1e4d2054e1163e39a06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989938833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf972a8f9ff2fce9f9ca75a08b35c399345e0347c096de0b4f53579fa7ad32d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:58:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 21:58:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 21:58:11 GMT
ENV NATS_SERVER=2.12.5
# Tue, 10 Mar 2026 21:58:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Tue, 10 Mar 2026 21:58:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.5/nats-server-v2.12.5-windows-amd64.zip
# Tue, 10 Mar 2026 21:58:14 GMT
ENV NATS_SERVER_SHASUM=29d6eca9ce085731bd63b32eeff7fae076938d31dd095acccfc70f2496d07ea7
# Tue, 10 Mar 2026 21:58:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 21:58:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 21:58:54 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 21:58:55 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 21:58:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 21:58:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04c32730da76e4f8c0992e8486404cface27cdbf86a7fe00437d3025590b7e`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02ad44b5ae354c11458cd62dee34cf93d9389058036580d4260d9551883ed0`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d2d6023a53e21e129bd012c45fed3f50dabc9d0bcea695e14ecdac1ad3f03`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0deaad7f12bcdc5138b621c8a8c2a35766f41f719b51f6add6f71d28a0842`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2a17f84ab038fcc41ab1c8aa33270d582ed981327779baf6d26e85c36b1f1c`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800dc056e1954416cde33967232d04ac013a4b298a04c3bb591bb6cda1a3696`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b556c3513211380357d8ba1d5774644200201d0a0973350c0b338eb7aecc6a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 484.7 KB (484712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e93160909732ff5d08e605284a33be5e2f51dd89a8ed9b5ad40bd5948a090`  
		Last Modified: Tue, 10 Mar 2026 21:59:04 GMT  
		Size: 7.2 MB (7159095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b56e0af4952401a1d938512f31f1e379baf7f63ec96da79f873f8cdf83c397`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d839d11021d15ecfbce6ae4d506186302258eabf46c50e87ce5c5b75ff02a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f70edc90f77cbdf7689415400d2da65bb2e9a269a97c7411d32ace56cba1ff`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5573ab3f95d8693954515f4dfd4b0a086da95b6c7456f05348de2e4c1eee1a2`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.6`

**does not exist** (yet?)

## `nats:2.12.6-alpine`

**does not exist** (yet?)

## `nats:2.12.6-alpine3.22`

**does not exist** (yet?)

## `nats:2.12.6-linux`

**does not exist** (yet?)

## `nats:2.12.6-nanoserver`

**does not exist** (yet?)

## `nats:2.12.6-nanoserver-ltsc2022`

**does not exist** (yet?)

## `nats:2.12.6-scratch`

**does not exist** (yet?)

## `nats:2.12.6-windowsservercore`

**does not exist** (yet?)

## `nats:2.12.6-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `nats:alpine`

```console
$ docker pull nats@sha256:c1379a8588df47244a4789ede85e8ae7490bd37006bde837e4d6fb6f559cb0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:f55092a58ef4b6883fd9b9e67c8741139c3701acff2d7e57930abbb54d2d4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10886061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81529466020c291e5ad80f56987ed653d491e1b9476ccbdeaf67b72affa3c278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8887a98e8249b73b0777bfbc8c0a30b02d3c21e3c39a9d768c5871b5585777`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 7.1 MB (7080215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dead58ebc17268f1b2f4cec215f560e3a07cc610d28eeff77d5f1c5d8e2517`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b4cd24f67b5d5afe059593810655b6887ba69dbdb160f71907e3daca8a8dc`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:685e730f881ec97c5e115e96bfe8066a26a611e53bcbfa4f0e69d4b4a174b46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb00ece4ca5cf51cc4d452e9249450fed5b54cfe2a9112947dca28d2ea8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3ba67a28104834d1d93b1e7e33ff17be9085f62d4b1100860816af7c9e0de`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c7bf3f984b3b64f0c1f9f4674a8f76c32e17a58c3a69291ad03b749fb8275ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52985b6ab22ea9e18f31378c7d723405b36c8533ab7e35049e80e606ec5042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148f12e063d142770b6e05b9f9c2ab014ab5763dff5f40cf43b4d8741dea20e0`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 6.8 MB (6797772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb32797a1c1b66b3d5d82193923eb3b39bbd560af58c01e71d7f46127eda32c`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c38be02f7f6968455354dfe4a4a05e5f20fbcdad07b63a3add2b522b3fc163`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7f5278fc819e312da44d7f8c6548fbd4f008b7047b81aaec0c88e1b6e7bf80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf1a9035fbf11bd94daf97ff6446b8c962f779e52915fdb47f723375a90161`

```dockerfile
```

-	Layers:
	-	`sha256:d069f32f6e0103cf7962bc3e50c1be2b0953ab9edcfb7db9f63defe80ce6c7b2`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de66d6fac8ce8ebef0e1032f68c75720b2d9fe3a040132c69bce4613ae04a5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10016287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb89708d609d7d7c02e11f18dbd6f2ebbd095aee4402d8d2d9a9c4ca7917e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627631ba1918c54c7a3365b569389ba221a3fcbd467f2f68c02834aa91cc94f`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 6.8 MB (6791688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909a283e1b0f458613bac969dccdc3e622f3167995890a9b73344d1afe42e0c`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc1d6c83015eb80bc6e00a18fd3fe4b50483b56a1b8d381db8551986ad949e`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a89cb4125128c4481995506bc126626436c2a4398b4d1ca640b05c513c9c3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576436877db30f3cde211a66a4c4013292cae5b6f4cdcba857a0f440e84397a8`

```dockerfile
```

-	Layers:
	-	`sha256:c681f3aa2919334b313a7f825221815da8a74b0c5717aece45a141747c4666a4`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ce72c5047aac010d13d69e087e2ef792ba483b581d3fe131a06f24f4bcd64499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10629509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78db93426f4ce81493b1740958536016471acce7c2469d30642d1ce5e2505028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825bb7632b2910036c4e99446261eaccf38a5407182667a9a5544165b29a3a66`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 6.5 MB (6489020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a075238f2783d207491918f497c4935823239fef8402991a1501e453f6dba`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e51ee93c455d52b0a680fe79d12a069061e5d506026beeda5e511a4b3221a49`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6803835c0dc24ce636ea74af20236401d626a7086072c838f1bdc957a100b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389309d70c5e974ba909c72462ccaecc37686be93ec78f5b3f4ec005cb0760b`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a9525024c9f083b6bf1027d0683e9da385aa15944aa3dd296418810f297b6`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:ea21e6eb9baed3f48d70928e28581f139ea88123ae96c10ab7fd753b196f711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6294e924a35b3ba351e1a9cb918458e4656b4bf790282e9b5b571ef60785615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:50 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f47dcf083e6405dbb62b78c40e89eddfa579782e18796398d04ac483723b67`  
		Last Modified: Mon, 09 Mar 2026 20:26:00 GMT  
		Size: 6.5 MB (6538200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cff225f6b222724626788da2eb98a26c2385e0464e86d59d843ae8cd9131b`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264d913d41a7e5acf68f5c7336a947d1c985b3beb40308165f5e1529c5e7e1`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c395e1e7cdcf166da464ce9b176a78f41cc1e379d12029384d18535e7510dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd1e702aa11e4a3b35ba6f6d3a008217124ef4d19d93d23e12767750a22642b`

```dockerfile
```

-	Layers:
	-	`sha256:1eed2a8cf66e0339f0d26be0f99591e27aa134d22ad734dce841c59737673453`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:922a66519e1e1d9166fcdf6ffc4ee018befd6cde9b8b53d7e614d2e41ed770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a50c0d0127f61de22b52cfc3acbf5c208e15f76b7a6e18a51e075465786d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:21 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a6cdb957401649789e5b4f2cbe88f55a7b8e0a8bd0609c92d9eef2c3a417e`  
		Last Modified: Mon, 09 Mar 2026 19:01:30 GMT  
		Size: 6.9 MB (6920512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7111270df9c5fff857ec52c3ba39df86a8800642c13f0d00bd04a1712b9d4e0`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919a6d79781833003c5f530b73820bdd56e515c4670f1a782d6f68bd6cbaf8d`  
		Last Modified: Mon, 09 Mar 2026 19:01:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dd1073397e51e35ad7dd3e192c8a292dede602bcea951e4d02a8e2acc25cc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f173e09372d1c0d616aa2b5e814f124a00b622196f5122bbe8ceb997b7f93d`

```dockerfile
```

-	Layers:
	-	`sha256:f149e96bc2411d24ddb1f3bd40351a3b5649c09c2f17f7db57ca653a6e4731ee`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:c1379a8588df47244a4789ede85e8ae7490bd37006bde837e4d6fb6f559cb0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:f55092a58ef4b6883fd9b9e67c8741139c3701acff2d7e57930abbb54d2d4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10886061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81529466020c291e5ad80f56987ed653d491e1b9476ccbdeaf67b72affa3c278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8887a98e8249b73b0777bfbc8c0a30b02d3c21e3c39a9d768c5871b5585777`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 7.1 MB (7080215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dead58ebc17268f1b2f4cec215f560e3a07cc610d28eeff77d5f1c5d8e2517`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b4cd24f67b5d5afe059593810655b6887ba69dbdb160f71907e3daca8a8dc`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:685e730f881ec97c5e115e96bfe8066a26a611e53bcbfa4f0e69d4b4a174b46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb00ece4ca5cf51cc4d452e9249450fed5b54cfe2a9112947dca28d2ea8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3ba67a28104834d1d93b1e7e33ff17be9085f62d4b1100860816af7c9e0de`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c7bf3f984b3b64f0c1f9f4674a8f76c32e17a58c3a69291ad03b749fb8275ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52985b6ab22ea9e18f31378c7d723405b36c8533ab7e35049e80e606ec5042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148f12e063d142770b6e05b9f9c2ab014ab5763dff5f40cf43b4d8741dea20e0`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 6.8 MB (6797772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb32797a1c1b66b3d5d82193923eb3b39bbd560af58c01e71d7f46127eda32c`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c38be02f7f6968455354dfe4a4a05e5f20fbcdad07b63a3add2b522b3fc163`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7f5278fc819e312da44d7f8c6548fbd4f008b7047b81aaec0c88e1b6e7bf80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf1a9035fbf11bd94daf97ff6446b8c962f779e52915fdb47f723375a90161`

```dockerfile
```

-	Layers:
	-	`sha256:d069f32f6e0103cf7962bc3e50c1be2b0953ab9edcfb7db9f63defe80ce6c7b2`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:de66d6fac8ce8ebef0e1032f68c75720b2d9fe3a040132c69bce4613ae04a5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10016287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb89708d609d7d7c02e11f18dbd6f2ebbd095aee4402d8d2d9a9c4ca7917e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627631ba1918c54c7a3365b569389ba221a3fcbd467f2f68c02834aa91cc94f`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 6.8 MB (6791688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909a283e1b0f458613bac969dccdc3e622f3167995890a9b73344d1afe42e0c`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc1d6c83015eb80bc6e00a18fd3fe4b50483b56a1b8d381db8551986ad949e`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a89cb4125128c4481995506bc126626436c2a4398b4d1ca640b05c513c9c3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576436877db30f3cde211a66a4c4013292cae5b6f4cdcba857a0f440e84397a8`

```dockerfile
```

-	Layers:
	-	`sha256:c681f3aa2919334b313a7f825221815da8a74b0c5717aece45a141747c4666a4`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ce72c5047aac010d13d69e087e2ef792ba483b581d3fe131a06f24f4bcd64499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10629509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78db93426f4ce81493b1740958536016471acce7c2469d30642d1ce5e2505028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825bb7632b2910036c4e99446261eaccf38a5407182667a9a5544165b29a3a66`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 6.5 MB (6489020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a075238f2783d207491918f497c4935823239fef8402991a1501e453f6dba`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e51ee93c455d52b0a680fe79d12a069061e5d506026beeda5e511a4b3221a49`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6803835c0dc24ce636ea74af20236401d626a7086072c838f1bdc957a100b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389309d70c5e974ba909c72462ccaecc37686be93ec78f5b3f4ec005cb0760b`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a9525024c9f083b6bf1027d0683e9da385aa15944aa3dd296418810f297b6`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ea21e6eb9baed3f48d70928e28581f139ea88123ae96c10ab7fd753b196f711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6294e924a35b3ba351e1a9cb918458e4656b4bf790282e9b5b571ef60785615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:50 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f47dcf083e6405dbb62b78c40e89eddfa579782e18796398d04ac483723b67`  
		Last Modified: Mon, 09 Mar 2026 20:26:00 GMT  
		Size: 6.5 MB (6538200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cff225f6b222724626788da2eb98a26c2385e0464e86d59d843ae8cd9131b`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264d913d41a7e5acf68f5c7336a947d1c985b3beb40308165f5e1529c5e7e1`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c395e1e7cdcf166da464ce9b176a78f41cc1e379d12029384d18535e7510dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd1e702aa11e4a3b35ba6f6d3a008217124ef4d19d93d23e12767750a22642b`

```dockerfile
```

-	Layers:
	-	`sha256:1eed2a8cf66e0339f0d26be0f99591e27aa134d22ad734dce841c59737673453`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:922a66519e1e1d9166fcdf6ffc4ee018befd6cde9b8b53d7e614d2e41ed770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a50c0d0127f61de22b52cfc3acbf5c208e15f76b7a6e18a51e075465786d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:21 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a6cdb957401649789e5b4f2cbe88f55a7b8e0a8bd0609c92d9eef2c3a417e`  
		Last Modified: Mon, 09 Mar 2026 19:01:30 GMT  
		Size: 6.9 MB (6920512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7111270df9c5fff857ec52c3ba39df86a8800642c13f0d00bd04a1712b9d4e0`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919a6d79781833003c5f530b73820bdd56e515c4670f1a782d6f68bd6cbaf8d`  
		Last Modified: Mon, 09 Mar 2026 19:01:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:dd1073397e51e35ad7dd3e192c8a292dede602bcea951e4d02a8e2acc25cc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f173e09372d1c0d616aa2b5e814f124a00b622196f5122bbe8ceb997b7f93d`

```dockerfile
```

-	Layers:
	-	`sha256:f149e96bc2411d24ddb1f3bd40351a3b5649c09c2f17f7db57ca653a6e4731ee`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:7971c76fcd4057c090faf5bc7673199ffe0ae586704518e9a469f156155b4e47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4893; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:4381ef3a8a655e7f0cca77861aa1b12801161df68c13147da4629b7bbdc1201e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:4e65924c3379e91937053a1f79ed9a3a79bf8a7bb5b38caca931059d70656eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4e65924c3379e91937053a1f79ed9a3a79bf8a7bb5b38caca931059d70656eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:8e31e937f82326a417e35e8e30befaf82bf0f0e8f4b2451fd83270edebecb573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133467209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91249cdaf6cf194b7ae26137df39b1e79bc95e7de677bf2b6add864f6d58ec7a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:35:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 22:35:49 GMT
RUN cmd /S /C #(nop) COPY file:43ca0d983360e736f84645c39fd7ae598025f6a645ae4c2ce4b8bae51bced147 in C:\nats-server.exe 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 22:35:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 22:35:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096acfd9b30f863c8a2b11e1133bab3c70549b10852e87b5e91cc9e5bae14a96`  
		Last Modified: Tue, 10 Mar 2026 22:35:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d567f4890bfdb7f8ecb4d364dfa2553d4d681c13f2eaddde6eb38f8fcc9fa7`  
		Last Modified: Tue, 10 Mar 2026 22:35:56 GMT  
		Size: 6.8 MB (6810724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038dbe0833497cbbcc303fa4f5d2cfc0b5aebfbdd30e4ad1b575a18205c2997`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fae83a6af8bd693e5e0dc53e075408be270ecdeff5505c9d35d3c7ba0f0f278`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708662d9c0f3d25bff6ad8560e72986c76e8910242c3af6adb0d9d60e3daa45`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c9aae6e572622ccb1e6484e3b6c422f1e27d703486d63d4bb89bec619af444`  
		Last Modified: Tue, 10 Mar 2026 22:35:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:4381ef3a8a655e7f0cca77861aa1b12801161df68c13147da4629b7bbdc1201e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:fedcbeab5b29480be0360a87e155368c87081e636a969f36d0746415e9e5d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6622434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293380ef259544d054c7185aeab374a5a1a68146602771d62bb23e5a6fa9b408`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dc5cd93f936a8192572142583d5de8ef78ad337c31c33613c1a2b45110a022b7`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.6 MB (6621925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c6fd4e728c9a9a8aaaf0b685d0e2dd85440cb2f679b2b6a947864dfe0f419`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:660cadd49c1c611d6c7953a3621ca15ee0aa12ee821105fca4dd96d09ab8779a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ac7c9d2a6761705cb9d0d8afd17125ebef03dc46972c602c2b09b47a71f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:409d255545cafed479b5ced068b17b1906f3aa881096fb8385a150e66011ae33`  
		Last Modified: Mon, 09 Mar 2026 19:12:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce306d87cf91205de5569936cbb5fac8a0349fd2295a3c4b3c33cf865fcaa998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a294532905e838c48c91042adef7a6168dbd884deab24c7129afa829b0737de`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:49:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:49:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7b493eab69cf8d337433317b0effe13dd301c6a4cc1eb60aadcccd5911d76ec`  
		Last Modified: Mon, 09 Mar 2026 16:09:52 GMT  
		Size: 6.3 MB (6342033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5758b76c6a327f7eb10984311ca3c6f77271d2aaa2dcf54c6fd55205d26793`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d210140ed309b8c6a3c4d3c3e0a562d39f200115906ea0edf4a40eae6d3999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5795f7e9a3d759fe6ef6f3e038baeab983a827c3ab311d4720b3eb62e5660870`

```dockerfile
```

-	Layers:
	-	`sha256:779e4b968464218f084a70332e614c5c00fb8479c40b0bb2f1a22673558bedd8`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:56b654dfc9ae27f27a572bf266e147ebd4207ebe5c022a435cebb5e7fa6c8100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf41da1cd69a6878652c5494fc30b29620e034d217fdf0c0493bce2a93589c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 21:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 21:53:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 21:53:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 21:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 21:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2c43d8b88ef868399d1e96fcd2acfebbd47abb8f11afe2933d4e3223d18db121`  
		Last Modified: Mon, 09 Mar 2026 16:09:47 GMT  
		Size: 6.3 MB (6329608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8fa481a758971a1d6d9fa725ae56e532efe884b5c1221811fbdbc4cdcfa23`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8bfdc08d73e992cabe47868b773e19a936e9c8511b8cf41fcf658611410b0023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d7d8d41df60c6074ab1b117b369c570b7a3e6d9a5db4b3927d1f26155991d`

```dockerfile
```

-	Layers:
	-	`sha256:95e9e70e996fc381c2b6df74bde7067540be1dfbefbcc088f41b3ce889317328`  
		Last Modified: Mon, 09 Mar 2026 21:53:16 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cdbce1e5fa894f534cff4189589e1ec55892be7989a0f3ec78a125ce78b304df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6030853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76b57e06193cf93eb973934ad8431bb3b62e6b487e2148d8e6e10beb75545e6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:51:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:51:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:51:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:51:27 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:51:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ade97a139f345619ea7078315b34cb2d5f104531166c6cf44ddbb1bda611d094`  
		Last Modified: Mon, 09 Mar 2026 16:09:48 GMT  
		Size: 6.0 MB (6030343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f5dd0be2f5559d8d5034a21476c12b6fdc778bdfc5aa03c2c976e4166db46`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d156810b94866eb5e6e3472b3f3def5ae0f987e4646e69ed8d7f2f8ba10a0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad2c657272745165fa9493e0ac6759e5c5484a4947d3041486d8b51f8b1783`

```dockerfile
```

-	Layers:
	-	`sha256:b1aa42d9f7f1e4447eea74ab50a754c6c68a3a14a9e84605e0c3b3965783834e`  
		Last Modified: Mon, 09 Mar 2026 19:51:31 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:bded1b6c1b1872230a52aa853337d24a84a77e454ea45f6261b9ad42e611ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2914575969d25b67c25804003a700e76d169a66ef2ab4add39ee86de10aa21`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 20:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 20:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:39:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:39:21 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 20:39:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e9b2e61eb237ba6a2fbecbee95b7e68d1ccbe54fbebfd226482452d95e16ee8b`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.1 MB (6078101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595871a1e46fdc2c458affe9d09f97b51b21c8fd060d461f0369a7896ab5f119`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a1122a5c19d6ba0a847197e50fc844a625a8c23d36e746a97bfcd3f43a92ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6a1cf3b0915a5e09761373e8980152fbb97caefb20ab911e66f54f0450b492`

```dockerfile
```

-	Layers:
	-	`sha256:3ba2b177643943bf3802e172ec7dc8a13332406618491c32dc2487a480ac7a25`  
		Last Modified: Mon, 09 Mar 2026 20:39:28 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:9eb6a0c9f8446df9abc2e3e20b92efc7241df6d98fffc64bd5e379f58a2a087d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc4ceddbd7477991bc520f47a7ebe6c59bd4d35f87dfe4b0ceda4c8bade7b9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 09 Mar 2026 19:11:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 09 Mar 2026 19:11:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:11:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:11:15 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 09 Mar 2026 19:11:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5d165a1f0f6b55da4769a5fc17b9452a00e33111d204c121cc1dd190b9a3afe4`  
		Last Modified: Mon, 09 Mar 2026 16:09:51 GMT  
		Size: 6.5 MB (6460897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db09a261a088f6f445fe0c64b1af801e1756cd4e8ed9a7c41efd54d7163212`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:eb7182e4b0a0772268dc0ec49df1ffa187d1bb15595d00100369303bb4fab943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171ce07b46824d8024651caa083ba2a7ce16d273af099579b83da3d80ec72b4a`

```dockerfile
```

-	Layers:
	-	`sha256:19d4a0205dd819109b88a36046fdb4501fef555cff4069921b4dc15213b2fb72`  
		Last Modified: Mon, 09 Mar 2026 19:11:23 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:9b0bc6e81344da3bd2751cf47d851dc71c28a7d7d30f7328b435c0d5083f3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:6ae257bf95b984fb32a4f6eeb280e11b127a5779eb61c1e4d2054e1163e39a06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989938833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf972a8f9ff2fce9f9ca75a08b35c399345e0347c096de0b4f53579fa7ad32d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:58:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 21:58:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 21:58:11 GMT
ENV NATS_SERVER=2.12.5
# Tue, 10 Mar 2026 21:58:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Tue, 10 Mar 2026 21:58:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.5/nats-server-v2.12.5-windows-amd64.zip
# Tue, 10 Mar 2026 21:58:14 GMT
ENV NATS_SERVER_SHASUM=29d6eca9ce085731bd63b32eeff7fae076938d31dd095acccfc70f2496d07ea7
# Tue, 10 Mar 2026 21:58:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 21:58:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 21:58:54 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 21:58:55 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 21:58:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 21:58:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04c32730da76e4f8c0992e8486404cface27cdbf86a7fe00437d3025590b7e`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02ad44b5ae354c11458cd62dee34cf93d9389058036580d4260d9551883ed0`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d2d6023a53e21e129bd012c45fed3f50dabc9d0bcea695e14ecdac1ad3f03`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0deaad7f12bcdc5138b621c8a8c2a35766f41f719b51f6add6f71d28a0842`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2a17f84ab038fcc41ab1c8aa33270d582ed981327779baf6d26e85c36b1f1c`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800dc056e1954416cde33967232d04ac013a4b298a04c3bb591bb6cda1a3696`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b556c3513211380357d8ba1d5774644200201d0a0973350c0b338eb7aecc6a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 484.7 KB (484712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e93160909732ff5d08e605284a33be5e2f51dd89a8ed9b5ad40bd5948a090`  
		Last Modified: Tue, 10 Mar 2026 21:59:04 GMT  
		Size: 7.2 MB (7159095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b56e0af4952401a1d938512f31f1e379baf7f63ec96da79f873f8cdf83c397`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d839d11021d15ecfbce6ae4d506186302258eabf46c50e87ce5c5b75ff02a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f70edc90f77cbdf7689415400d2da65bb2e9a269a97c7411d32ace56cba1ff`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5573ab3f95d8693954515f4dfd4b0a086da95b6c7456f05348de2e4c1eee1a2`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:9b0bc6e81344da3bd2751cf47d851dc71c28a7d7d30f7328b435c0d5083f3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:6ae257bf95b984fb32a4f6eeb280e11b127a5779eb61c1e4d2054e1163e39a06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989938833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf972a8f9ff2fce9f9ca75a08b35c399345e0347c096de0b4f53579fa7ad32d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:58:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 21:58:10 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Mar 2026 21:58:11 GMT
ENV NATS_SERVER=2.12.5
# Tue, 10 Mar 2026 21:58:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Tue, 10 Mar 2026 21:58:13 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.5/nats-server-v2.12.5-windows-amd64.zip
# Tue, 10 Mar 2026 21:58:14 GMT
ENV NATS_SERVER_SHASUM=29d6eca9ce085731bd63b32eeff7fae076938d31dd095acccfc70f2496d07ea7
# Tue, 10 Mar 2026 21:58:36 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Mar 2026 21:58:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Mar 2026 21:58:54 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 10 Mar 2026 21:58:55 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Mar 2026 21:58:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Mar 2026 21:58:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04c32730da76e4f8c0992e8486404cface27cdbf86a7fe00437d3025590b7e`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02ad44b5ae354c11458cd62dee34cf93d9389058036580d4260d9551883ed0`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d2d6023a53e21e129bd012c45fed3f50dabc9d0bcea695e14ecdac1ad3f03`  
		Last Modified: Tue, 10 Mar 2026 21:59:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0deaad7f12bcdc5138b621c8a8c2a35766f41f719b51f6add6f71d28a0842`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2a17f84ab038fcc41ab1c8aa33270d582ed981327779baf6d26e85c36b1f1c`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800dc056e1954416cde33967232d04ac013a4b298a04c3bb591bb6cda1a3696`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b556c3513211380357d8ba1d5774644200201d0a0973350c0b338eb7aecc6a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:02 GMT  
		Size: 484.7 KB (484712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e93160909732ff5d08e605284a33be5e2f51dd89a8ed9b5ad40bd5948a090`  
		Last Modified: Tue, 10 Mar 2026 21:59:04 GMT  
		Size: 7.2 MB (7159095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b56e0af4952401a1d938512f31f1e379baf7f63ec96da79f873f8cdf83c397`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d839d11021d15ecfbce6ae4d506186302258eabf46c50e87ce5c5b75ff02a5`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f70edc90f77cbdf7689415400d2da65bb2e9a269a97c7411d32ace56cba1ff`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5573ab3f95d8693954515f4dfd4b0a086da95b6c7456f05348de2e4c1eee1a2`  
		Last Modified: Tue, 10 Mar 2026 21:59:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
