<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.4`](#nats214)
-	[`nats:2.1.4-alpine`](#nats214-alpine)
-	[`nats:2.1.4-alpine3.11`](#nats214-alpine311)
-	[`nats:2.1.4-linux`](#nats214-linux)
-	[`nats:2.1.4-nanoserver`](#nats214-nanoserver)
-	[`nats:2.1.4-nanoserver-1809`](#nats214-nanoserver-1809)
-	[`nats:2.1.4-scratch`](#nats214-scratch)
-	[`nats:2.1.4-windowsservercore`](#nats214-windowsservercore)
-	[`nats:2.1.4-windowsservercore-1809`](#nats214-windowsservercore-1809)
-	[`nats:2.1.4-windowsservercore-ltsc2016`](#nats214-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.11`](#nats21-alpine311)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.11`](#nats2-alpine311)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.11`](#natsalpine311)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:f3d9542f19076b2fbcfd1228fabcd59dee47dbcb80ae01ba1ad6a9a9eb28df0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1098; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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

### `nats:2` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:f3d9542f19076b2fbcfd1228fabcd59dee47dbcb80ae01ba1ad6a9a9eb28df0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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

### `nats:2.1` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4`

```console
$ docker pull nats@sha256:1400dc276cd5fcdf029f372b45730010727052009c58878a03c0e4916f2e170f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.4` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-linux`

```console
$ docker pull nats@sha256:59d691ed3578e01695053510d3128c00f9d1676b5a4965bdb048a78aed1e4bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-nanoserver`

```console
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.4-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-nanoserver-1809`

```console
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.4-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-scratch`

```console
$ docker pull nats@sha256:59d691ed3578e01695053510d3128c00f9d1676b5a4965bdb048a78aed1e4bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-windowsservercore`

```console
$ docker pull nats@sha256:32ceb99f7382c12265666a7eb0d3b757fef5e8a0e1188c42d39e77d3f8d81849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3506; amd64

### `nats:2.1.4-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.4-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:8aa9f80a9cdac9b90b9d647a4b847c2a5901c9b0ff5ceb75a919be33083ba394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1.4-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.4-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f62e1d7ec98a964e65d17f59e580066dda46503085e6c27a4c455e235bc876ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `nats:2.1.4-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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
$ docker pull nats@sha256:32ceb99f7382c12265666a7eb0d3b757fef5e8a0e1188c42d39e77d3f8d81849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3506; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:8aa9f80a9cdac9b90b9d647a4b847c2a5901c9b0ff5ceb75a919be33083ba394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f62e1d7ec98a964e65d17f59e580066dda46503085e6c27a4c455e235bc876ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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
$ docker pull nats@sha256:32ceb99f7382c12265666a7eb0d3b757fef5e8a0e1188c42d39e77d3f8d81849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3506; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:8aa9f80a9cdac9b90b9d647a4b847c2a5901c9b0ff5ceb75a919be33083ba394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f62e1d7ec98a964e65d17f59e580066dda46503085e6c27a4c455e235bc876ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.11`

```console
$ docker pull nats@sha256:2e2b05fb1b4fc71226dc1c91272d0f9fd4bf65f6d6471083ff37486844950e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:a32637b269186be7992776abdb9ce5d7d746c00e391e57785332ec836e5d7e29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099edd8b94f01851d38938e11840b6957c3a2b528c37af6bc76ff9ad08858efc`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:31:44 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:31:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:31:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:31:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:31:46 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50105b0b1f19f0bb4d67cd730963c156d1cd742b03fc121f67d8b257cfbcd7`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 4.4 MB (4353819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f28704fb98ac80698c603bf4a9831765b35217cee595b5526578eea2660f1b8`  
		Last Modified: Thu, 30 Jan 2020 23:32:32 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:b089d22b361adda1e1f900655b7e68ac2004b5dc4101e4fe83967139de9d3490
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2c31e13d7818401488d0b4b2f002e9b98c6988f4039f4a00ce3c8de986d7`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 22:51:36 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 22:51:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 22:51:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 22:51:42 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:51:43 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e33b0b488e7087deb3f7d6af232eb94b62b0b35156668f00c65490c580f1348`  
		Last Modified: Thu, 30 Jan 2020 22:52:40 GMT  
		Size: 4.1 MB (4066830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f644e5c63045808ac35c523b86edaf434d077083d2eb56324914b54d75c4dc0`  
		Last Modified: Thu, 30 Jan 2020 22:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:3240fbb0ad0a9ab99cf4bf5aa2ec46471286688cd6c4eee30488eef9629147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cebe9fc98c6895e3a05cc374c42a84da318a1d30c2c9b4d3859df218a838631`
-	Default Command: `["nats-server"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2020 23:40:22 GMT
ENV NATS_SERVER=2.1.4
# Thu, 30 Jan 2020 23:40:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 30 Jan 2020 23:40:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 30 Jan 2020 23:40:28 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:40:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe342b712fb35d7804c65360827ec031c10c09a26b9a7e6704aa7e7d231a7465`  
		Last Modified: Thu, 30 Jan 2020 23:42:19 GMT  
		Size: 4.1 MB (4061188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931287b5be201e321ab484539979106b4730feed2aa5928561b5affc686e7920`  
		Last Modified: Thu, 30 Jan 2020 23:42:18 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:f3d9542f19076b2fbcfd1228fabcd59dee47dbcb80ae01ba1ad6a9a9eb28df0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1098; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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

### `nats:latest` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:68c919884163230b5923beda351648dcd3133ebd845105185f0f2b75ed8dc721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:dc3eee192e3630296ead55084895c5119e1f09a60cb59147601bd20de4cc043f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3e794e8ec657bb377b12ca1bf13eada56a2b721d5fee7595fc8812166fc77`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 22:52:17 GMT
COPY file:f5c65bd40159137e73ffdc2b2bd814940ba0730ffae9cf87fd239f4f0998ac6d in /nats-server 
# Thu, 30 Jan 2020 22:52:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 22:52:18 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 22:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 22:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a8a48b1fff28179cbbf2f509c1968a74eceef24ff2378b53e6e14f7ae1f7f0`  
		Last Modified: Thu, 30 Jan 2020 22:52:53 GMT  
		Size: 3.8 MB (3764506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdaa57a0d28a46144d3a397a4e5ce178e1aa519cecb8c72252c32c574886abb`  
		Last Modified: Thu, 30 Jan 2020 22:52:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
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
$ docker pull nats@sha256:32ceb99f7382c12265666a7eb0d3b757fef5e8a0e1188c42d39e77d3f8d81849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3506; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:8aa9f80a9cdac9b90b9d647a4b847c2a5901c9b0ff5ceb75a919be33083ba394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:63fc40f0e2573a4cc7a8561e7587546edaab4ca5b423960b57cf301082354d63
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278646261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388585ec11619cb6e50ba191a23880bc5f6932eb57d1945ce4dc0972d174f9d6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 14:45:12 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:45:13 GMT
ENV NATS_SERVER=2.1.4
# Wed, 11 Mar 2020 14:45:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Wed, 11 Mar 2020 14:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Mar 2020 14:46:54 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Wed, 11 Mar 2020 14:46:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:46:57 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:46:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ed96bfcc8cc17c8c1192c9f852f19ab1a2bcea7fa094f5e3f417f29b731f1e`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98ba99af1b58782702fe9eda4165ee874ae4a971d5520ad9b34107aa33676ee`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce9b96b32ea40df54ab10d8d099c2f9402a1e33841b3f8d8b91c4f4a00a4ce8`  
		Last Modified: Wed, 11 Mar 2020 14:48:09 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2736bd7ecebe10daf533502e987f537ad9bdfe824da8fd70dd863fa50ff38`  
		Last Modified: Wed, 11 Mar 2020 14:48:10 GMT  
		Size: 4.7 MB (4657611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a940a5ef35d1e6437b2c33be03506d2c421a8718d534317d9ff7d40dd956af`  
		Last Modified: Wed, 11 Mar 2020 14:48:08 GMT  
		Size: 8.6 MB (8642144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af24579375e6b5904240402285bfe91b73d12364d03d1e604e3d4d0a8f446b8`  
		Last Modified: Wed, 11 Mar 2020 14:48:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afe09e657b6da79ee8a576fcb8b9976110320286dd6fc124489c3116f8247d0`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad5438bdf0e237d1112fb3de34fa6af4611a470eacea342e365f8cccf9ed6c`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165c3e8e0b9d6bc5a24a8625afa7d2ecdeb8ef94279075658ee5332cf70e2082`  
		Last Modified: Wed, 11 Mar 2020 14:48:04 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f62e1d7ec98a964e65d17f59e580066dda46503085e6c27a4c455e235bc876ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull nats@sha256:219a891cab0de0ea10d533e263e12f07062bf2b2b896020ff7c47fb7f4d65bc3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5741810639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068fb26b880bb0034ec21dc3a20caf75dd7364577a97b80eb045d680b9086bfd`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:12:55 GMT
ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:12:56 GMT
ENV NATS_SERVER=2.1.4
# Thu, 20 Feb 2020 05:12:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.4/nats-server-v2.1.4-windows-amd64.zip
# Thu, 20 Feb 2020 05:14:07 GMT
RUN Set-PSDebug -Trace 2
# Thu, 20 Feb 2020 05:16:02 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Thu, 20 Feb 2020 05:16:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 20 Feb 2020 05:16:05 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Feb 2020 05:16:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 20 Feb 2020 05:16:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be123fd3da5da380246fee0dcb939ee80c14cdf77ddd79a2ecb888b2e7fd0418`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d62c822222a8f91702b5a919c531b3b2dfdd3feb05c9fa9812893beb31e5700`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd35f7808a193ef2ef43202b91408d3345468e768b6283e6eaeb94d8e40c5ee5`  
		Last Modified: Thu, 20 Feb 2020 05:18:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d1d06df8fb3e66a61d0097b075fe85d9c8d8b1f2499763de43d26b21187e08`  
		Last Modified: Thu, 20 Feb 2020 05:18:27 GMT  
		Size: 5.4 MB (5356595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ed83140ea5c990e93c5883e38b24d028d43875f1f8a52b76aa219658aa726`  
		Last Modified: Thu, 20 Feb 2020 05:18:28 GMT  
		Size: 9.4 MB (9379005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af5dda736d79d50ee1186291845bd13c8cc2932b1727ba1477ba39ddc594ac`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bce8a5ad304a7b363d2ad3d35131591a21e7e031d0d2b07d581d4116a982`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd29c8188523d7e056e74afc54b8e2f34a8261881166f25ac436b7cfb94178b`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00489777464bf003421423d8818255e66346104382aa71f1155e1e713a568846`  
		Last Modified: Thu, 20 Feb 2020 05:18:19 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
