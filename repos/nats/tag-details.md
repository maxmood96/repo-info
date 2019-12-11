<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.2`](#nats212)
-	[`nats:2.1.2-alpine`](#nats212-alpine)
-	[`nats:2.1.2-alpine3.10`](#nats212-alpine310)
-	[`nats:2.1.2-linux`](#nats212-linux)
-	[`nats:2.1.2-nanoserver`](#nats212-nanoserver)
-	[`nats:2.1.2-nanoserver-1803`](#nats212-nanoserver-1803)
-	[`nats:2.1.2-nanoserver-1809`](#nats212-nanoserver-1809)
-	[`nats:2.1.2-scratch`](#nats212-scratch)
-	[`nats:2.1.2-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.1.2-windowsservercore-1803`](#nats212-windowsservercore-1803)
-	[`nats:2.1.2-windowsservercore-1809`](#nats212-windowsservercore-1809)
-	[`nats:2.1.2-windowsservercore-ltsc2016`](#nats212-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.10`](#nats21-alpine310)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1803`](#nats21-nanoserver-1803)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1803`](#nats21-windowsservercore-1803)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.10`](#nats2-alpine310)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1803`](#nats2-nanoserver-1803)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1803`](#nats2-windowsservercore-1803)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.10`](#natsalpine310)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1803`](#natsnanoserver-1803)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1803`](#natswindowsservercore-1803)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:83922f11aa2012176cc23401cc1a7648c6d0aeecd1597e04c04d1028908d155c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:83922f11aa2012176cc23401cc1a7648c6d0aeecd1597e04c04d1028908d155c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2`

```console
$ docker pull nats@sha256:23f277004e8a26375011bd33abec3cd5e88aeeedf0642e15b373e918895ad7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1.2` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-alpine`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-alpine3.10`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.2-alpine3.10` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-alpine3.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-alpine3.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-linux`

```console
$ docker pull nats@sha256:5d778a5f18cfeef52e2e6676b2c6447fb21723e25ed25c65668d00f118b7c2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-nanoserver`

```console
$ docker pull nats@sha256:ad83801e139ed92e1c3900d7407335d26916c88c015f3ef8a177e4f22b6a9271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1.2-nanoserver` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-nanoserver` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-nanoserver-1803`

```console
$ docker pull nats@sha256:88e50a22cb8e8b38fd9c160baf274abfd70056270ad20d907027032bc6a35fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1.2-nanoserver-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-nanoserver-1809`

```console
$ docker pull nats@sha256:71bf025f0131d3ab0052913de0acda776986f6aa4af2308de0c9a2ec435fe7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:2.1.2-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-scratch`

```console
$ docker pull nats@sha256:5d778a5f18cfeef52e2e6676b2c6447fb21723e25ed25c65668d00f118b7c2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-windowsservercore`

```console
$ docker pull nats@sha256:bb8453d8412bb5c67ac9cd66f7bc527e02e5de89c6a569c562155fedd1031f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64
	-	windows version 10.0.14393.3384; amd64

### `nats:2.1.2-windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.2-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-windowsservercore-1803`

```console
$ docker pull nats@sha256:01aecc0fbccaba0900bf9857189a1720a3055f6973ac7cea656b09a42ed2bdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1.2-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:d143d9fbb4b0b4c0fe52c02ea6ce80517b3941a918445d8053d29b7220ea52a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:2.1.2-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:5152869192913a1fb2fc672d3d51c7215dcab6e6fa91506929f97afd40228b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `nats:2.1.2-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.10`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine3.10` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:59141670457fa112c6b1cf5cca3b159ad15bfb7e70fe0b1acbbb5616d922a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver`

```console
$ docker pull nats@sha256:ad83801e139ed92e1c3900d7407335d26916c88c015f3ef8a177e4f22b6a9271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-nanoserver` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1803`

```console
$ docker pull nats@sha256:88e50a22cb8e8b38fd9c160baf274abfd70056270ad20d907027032bc6a35fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1-nanoserver-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:71bf025f0131d3ab0052913de0acda776986f6aa4af2308de0c9a2ec435fe7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:59141670457fa112c6b1cf5cca3b159ad15bfb7e70fe0b1acbbb5616d922a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore`

```console
$ docker pull nats@sha256:bb8453d8412bb5c67ac9cd66f7bc527e02e5de89c6a569c562155fedd1031f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64
	-	windows version 10.0.14393.3384; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1803`

```console
$ docker pull nats@sha256:01aecc0fbccaba0900bf9857189a1720a3055f6973ac7cea656b09a42ed2bdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:2.1-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:d143d9fbb4b0b4c0fe52c02ea6ce80517b3941a918445d8053d29b7220ea52a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:5152869192913a1fb2fc672d3d51c7215dcab6e6fa91506929f97afd40228b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.10`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine3.10` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:59141670457fa112c6b1cf5cca3b159ad15bfb7e70fe0b1acbbb5616d922a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:ad83801e139ed92e1c3900d7407335d26916c88c015f3ef8a177e4f22b6a9271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-nanoserver` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1803`

```console
$ docker pull nats@sha256:88e50a22cb8e8b38fd9c160baf274abfd70056270ad20d907027032bc6a35fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:2-nanoserver-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:71bf025f0131d3ab0052913de0acda776986f6aa4af2308de0c9a2ec435fe7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:59141670457fa112c6b1cf5cca3b159ad15bfb7e70fe0b1acbbb5616d922a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:bb8453d8412bb5c67ac9cd66f7bc527e02e5de89c6a569c562155fedd1031f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64
	-	windows version 10.0.14393.3384; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1803`

```console
$ docker pull nats@sha256:01aecc0fbccaba0900bf9857189a1720a3055f6973ac7cea656b09a42ed2bdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:2-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:d143d9fbb4b0b4c0fe52c02ea6ce80517b3941a918445d8053d29b7220ea52a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:5152869192913a1fb2fc672d3d51c7215dcab6e6fa91506929f97afd40228b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.10`

```console
$ docker pull nats@sha256:980b72b10fc5b19053953540e34344b3c907ee171b7e88588ac7840cb4625b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine3.10` - linux; amd64

```console
$ docker pull nats@sha256:8080209e55d6b507a07f177de43a49b5508ce5e623d278490df1e43a311bb885
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301c08dadf72fdd3663e273cfbe85c67f2180a11982c76c93549c573df6b8ed`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 01:13:19 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 01:13:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 01:13:22 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 01:13:22 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:13:22 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cdb3689c6bca7ad32258e8f7a1d02c41a177ab3e0045870b82a6ccf27ba1c`  
		Last Modified: Wed, 20 Nov 2019 01:14:32 GMT  
		Size: 4.3 MB (4305309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d7533c6bab8302902b26aadbfc629dbd7d8cbe3ee5b95b17eccb10287163d1`  
		Last Modified: Wed, 20 Nov 2019 01:14:31 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:1f3d8a0e57c2563b44afd9090acbefdf5f0767b9c19676718a2c8ef2ded890d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6664423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b33ff58541789653dcb6bd4b8d77adf1a6736c9437724c330045cc61bf8af5`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2019 23:59:06 GMT
ENV NATS_SERVER=2.1.2
# Tue, 19 Nov 2019 23:59:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 19 Nov 2019 23:59:10 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 19 Nov 2019 23:59:11 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Nov 2019 23:59:12 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea71364ef454b26e11ff752a848a2082a52a04e4f6546440db8eabca6ce995`  
		Last Modified: Wed, 20 Nov 2019 00:05:05 GMT  
		Size: 4.1 MB (4092558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5cf1891da51ec7750e2dd9e60f71d4c94cf5938313cef32716ec440ce77228`  
		Last Modified: Wed, 20 Nov 2019 00:05:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:de426f19f9d38400b074a5c47eabab1091175917f5ad1a49d747f125c64601af
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5030ab20fc6f5fc08dc1e815bed30621a196d7c4e9080664c0a5f0f6a4715e68`
-	Default Command: `["nats-server"]`

```dockerfile
# Mon, 21 Oct 2019 18:15:18 GMT
ADD file:6b2893134302eabeb80e356fc4e5a29d9cd442362c382b3504688c014a734bb9 in / 
# Mon, 21 Oct 2019 18:15:31 GMT
CMD ["/bin/sh"]
# Wed, 20 Nov 2019 00:46:20 GMT
ENV NATS_SERVER=2.1.2
# Wed, 20 Nov 2019 00:46:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 20 Nov 2019 00:46:24 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 20 Nov 2019 00:46:24 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:46:25 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:99fc70ac0b64db67086f98ceb3942600816eed98046abd6be5ad66f4614a9ca2`  
		Last Modified: Mon, 21 Oct 2019 18:16:16 GMT  
		Size: 2.4 MB (2378437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9160be85eb7f1b4febc147ef0ef0e1b3ffbf31a7fffa29563c189655d0ee76bc`  
		Last Modified: Wed, 20 Nov 2019 00:53:54 GMT  
		Size: 4.1 MB (4087662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db07fe958ca47bfcc6434e62c2ec2bb24369d94f73c137e7c45640b6959c82`  
		Last Modified: Wed, 20 Nov 2019 00:53:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:83922f11aa2012176cc23401cc1a7648c6d0aeecd1597e04c04d1028908d155c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:59141670457fa112c6b1cf5cca3b159ad15bfb7e70fe0b1acbbb5616d922a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:ad83801e139ed92e1c3900d7407335d26916c88c015f3ef8a177e4f22b6a9271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64

### `nats:nanoserver` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:nanoserver` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1803`

```console
$ docker pull nats@sha256:88e50a22cb8e8b38fd9c160baf274abfd70056270ad20d907027032bc6a35fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:nanoserver-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:4273348c61d8b64416ca03627b111efa6b4f675e0ce4e95987687d18d449b727
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157218109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88c846d46969d608f0b476efb04c4cdffdc2c3dbb117655c8929c24647a501d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:30 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:35 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da11b096a0a0e65d1b9a889cec79631bb59332b8c187db3eeaf23e87a19542d`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 4.0 MB (3988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded9fb91d09e8ee7ad3a267026a5daac2397c246c18d4773cfe82f6689640021`  
		Last Modified: Wed, 11 Dec 2019 18:34:12 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace34606f3f817f7dd804c5998e97fed4e27386dc7b76730fa8c105a8cd89acd`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7aa2a04bbc4813cca8ebfe0692d10a77261b06ba9a5ea82810b6382750ae4`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107f619610c631793cf5a70649c930dd0c09a3503400d6d02cefe52c7545a0f8`  
		Last Modified: Wed, 11 Dec 2019 18:34:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:71bf025f0131d3ab0052913de0acda776986f6aa4af2308de0c9a2ec435fe7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:59141670457fa112c6b1cf5cca3b159ad15bfb7e70fe0b1acbbb5616d922a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:8139c5bf4df6e8635cb3420d2dfab08ecdf75b8d16cd82c40a67bd4417b2e71c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49014ccb53efc06dc1ce6656aea0abf000881d9db3ac5b31c6f8aef934452b30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:f7ba6139c8151888be538812698c1aab4311e97fcfac3b5af13138cd7d7e1405 in /nats-server 
# Wed, 20 Nov 2019 01:14:07 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 01:14:08 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 01:14:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 01:14:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f3c8f35bd9bcd03ff8eba7551a59aa4fb56c5eabac4758b0b6cb12709785f25c`  
		Last Modified: Wed, 20 Nov 2019 01:14:44 GMT  
		Size: 4.0 MB (4002195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba25f2430b4efc5a2c8e36c142c7aca0b9a14a6caf16fe09d29f97f77f4efce`  
		Last Modified: Wed, 20 Nov 2019 01:14:43 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:234935205b93b7c99b67d82fe35226290aa302e2b35b32f7f9516aa770bf6003
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f838f1a59cd8673948823057d50b486bb443ce5318e5a24502ded16334feda`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:04:38 GMT
COPY file:1c509c11a9e5697ac3184dd6c0dca46386d2a5d22fabbd0f4898bad8342884d8 in /nats-server 
# Wed, 20 Nov 2019 00:04:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:04:39 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:04:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:04:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ab4822bfc4bb3725c051563099752bf9f3cc14db9a698a66f64c906201e88b2d`  
		Last Modified: Wed, 20 Nov 2019 00:05:19 GMT  
		Size: 3.8 MB (3789828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9cf11d4796d35bb8140733b85f1398c199c592ad417cb6d22eac97b0ac377`  
		Last Modified: Wed, 20 Nov 2019 00:05:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:92ea09078a55fc56a807ede1630a862d4b6acc12633391a5a42b41483c6b66fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b97d154301cbefd42558306e1ece9667269fb9bda4c0ff2c2f601b578c2c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 20 Nov 2019 00:53:13 GMT
COPY file:f7bd56432332a04229b22e2b4ed52b31e5ba863bb47a2aacf6d808bd4a8397d1 in /nats-server 
# Wed, 20 Nov 2019 00:53:14 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 20 Nov 2019 00:53:15 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Nov 2019 00:53:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 20 Nov 2019 00:53:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:27216bfb43f9e231372de919d3bbc108e604422a1019a0b0407001997c0575fe`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 3.8 MB (3786237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3750c7c4312b8b2af995298314a15791a97ce1ef156b81c0477e579fb42b7f2e`  
		Last Modified: Wed, 20 Nov 2019 00:54:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:bb8453d8412bb5c67ac9cd66f7bc527e02e5de89c6a569c562155fedd1031f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1184; amd64
	-	windows version 10.0.14393.3384; amd64

### `nats:windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1803`

```console
$ docker pull nats@sha256:01aecc0fbccaba0900bf9857189a1720a3055f6973ac7cea656b09a42ed2bdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats:windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats@sha256:8d1394d4f2586a41dcbde8b9fd4614db9d4d98d4a6068c90cca278762422a33c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370299684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598c8951572c322c90229487e8d0bb71106ce065df0d05ea2717164d6b8dc936`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:25:55 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:25:56 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:25:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:26:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:28:03 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:28:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:28:05 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:28:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:28:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0fcc6f597904ec5ed4a706026a53ae4f49b0c4403a2ad32bcffffef74a098d`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32f52d2be0386946a41c3545a20c11d0fa83307e8a990c5321170376fea24f`  
		Last Modified: Wed, 11 Dec 2019 18:33:31 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484e976dc1a2f1dfc0b302ff83b6f00bae4626b1330c7cc63d7c0f7a9f1a1c56`  
		Last Modified: Wed, 11 Dec 2019 18:33:32 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d9622e2321945cae6465f3dd630fddd302120e3d818a330993729b8917ce4`  
		Last Modified: Wed, 11 Dec 2019 18:33:33 GMT  
		Size: 4.9 MB (4887442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec317fadd39572048352ae32467514419317b35bd72d1e0ce7635bb5edb2e1c`  
		Last Modified: Wed, 11 Dec 2019 18:33:34 GMT  
		Size: 8.8 MB (8840350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f202fe95f354af858faa79537de9ced45bcdf9a87b2ab20f6d003810bf033096`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305db9f7c12c732c7907ecbcd75a03a78e975c9187666d854bd0cdf0edd913b0`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ef83dbdfe3dd965d8344e40e07fa7c2deaa3e4b52f01f2a24916460c2d9aa1`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c871b6d043d414ed7fbf5efecca238d8cca52defd284399e884d21b6374d2a`  
		Last Modified: Wed, 11 Dec 2019 18:33:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:d143d9fbb4b0b4c0fe52c02ea6ce80517b3941a918445d8053d29b7220ea52a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:8695bfbe190624bb49dbacf2767ff9fe07ab06422dd496729462e65a0eb56163
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229422573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708cd504c572d596223e163f3f123a37a7063958791895a990d4c0527374f81f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Wed, 11 Dec 2019 14:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:23:50 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:23:52 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:23:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:24:34 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:25:38 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:25:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:25:40 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:25:42 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:25:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6095b83882ccf9b8fa968e24adeb7b300cf94138c6c34f21c5d0425dc8a63803`  
		Last Modified: Wed, 11 Dec 2019 17:59:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bfc31cc1d6689ebcc794ca795d6863008d588fb58098bf49718e1c95311fa`  
		Last Modified: Wed, 11 Dec 2019 18:32:47 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a17f634b9f04fb2b01c0eea2f5ab18d0b62a7a4834efc8ffe5db1e6aee5310`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d27ee737d70e216b7a16a3d38df258d540e106de9617f5a4b81a3ca06faa48`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eca62560c65a1777d29f1135f137eb4cd135f949945cb1fbbb73a7ee5a868`  
		Last Modified: Wed, 11 Dec 2019 18:32:50 GMT  
		Size: 4.6 MB (4579739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5a8a3b69f4dd6d3719dd4e52bedebb7859cc8c9ba8b8f6f42e50f66ce3993b`  
		Last Modified: Wed, 11 Dec 2019 18:32:46 GMT  
		Size: 8.5 MB (8529444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f4ff6fea0aa9033ba6fb25adaada94ddbe1e7fb3b82b3ebb9231fa2c1a47eb`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b55c626ec98a1131a7587023e14cef2a1337996e25f85c82331dc0644e5a22`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531969eaaaf4369ad4c576d4862c71e0cc520537edd7744a70f7bc65372feb3b`  
		Last Modified: Wed, 11 Dec 2019 18:32:44 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9a9d61fc03794eb6005d554c25cbcb1286b9699fef11fe0be5e851ad72fe75`  
		Last Modified: Wed, 11 Dec 2019 18:32:43 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:5152869192913a1fb2fc672d3d51c7215dcab6e6fa91506929f97afd40228b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats@sha256:9504d07894b580a2fb99be201c641164e28693fa7c2867df37fcf9af9a47786f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5737430879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6658cfedaecfeab92b158f20ca7aa71545cc3a1d80a764e1f7b8490675dcf4df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 18:28:48 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:28:49 GMT
ENV NATS_SERVER=2.1.2
# Wed, 11 Dec 2019 18:28:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.2/nats-server-v2.1.2-windows-amd64.zip
# Wed, 11 Dec 2019 18:29:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2019 18:31:26 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Dec 2019 18:31:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:29 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:30 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:31:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa11fca135b9d60cf92ac2ccd0a9c4cacd6c45bb607b33b786e27aad02d0a74`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b842ca9abad8f34dd3d712250bdbe2c87fd93732a92681202f4e100bd4e8e3`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227678cc0ef2c8f3f87e09fd25fd1946578a73d85ecf8db095a6b5e9b0d69e00`  
		Last Modified: Wed, 11 Dec 2019 18:34:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44efe6d263710e7df5e1a9d3ec9484256c5142a574e0f3bbbd4b4c22103c5f6`  
		Last Modified: Wed, 11 Dec 2019 18:34:55 GMT  
		Size: 5.4 MB (5362286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073385b46342a6e9b9307a07a82e3bc1e9608c1abd37e4759b999e18282672a`  
		Last Modified: Wed, 11 Dec 2019 18:34:54 GMT  
		Size: 9.4 MB (9354624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb99a78ed2ca0c9a9bbf4782f2d505d9cf39e456031b8d324d7752f39fd1136`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ff97d636e1e97e91be8221a986b6b37e94cf2725ce56417d19fa542ecaee8`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f570bd7d7278eb21a1c121861c889f17fe6f3f6994ad09706303d5e6cea88f`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafcc2a2ef8ed11d0cf04f9a6d5f865c624525b958123598ef36ad82255ea5d3`  
		Last Modified: Wed, 11 Dec 2019 18:34:51 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
