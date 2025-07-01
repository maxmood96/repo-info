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
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.22`](#nats210-alpine322)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-ltsc2022`](#nats210-nanoserver-ltsc2022)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-ltsc2022`](#nats210-windowsservercore-ltsc2022)
-	[`nats:2.10.29`](#nats21029)
-	[`nats:2.10.29-alpine`](#nats21029-alpine)
-	[`nats:2.10.29-alpine3.22`](#nats21029-alpine322)
-	[`nats:2.10.29-linux`](#nats21029-linux)
-	[`nats:2.10.29-nanoserver`](#nats21029-nanoserver)
-	[`nats:2.10.29-nanoserver-ltsc2022`](#nats21029-nanoserver-ltsc2022)
-	[`nats:2.10.29-scratch`](#nats21029-scratch)
-	[`nats:2.10.29-windowsservercore`](#nats21029-windowsservercore)
-	[`nats:2.10.29-windowsservercore-ltsc2022`](#nats21029-windowsservercore-ltsc2022)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.22`](#nats211-alpine322)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-ltsc2022`](#nats211-nanoserver-ltsc2022)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-ltsc2022`](#nats211-windowsservercore-ltsc2022)
-	[`nats:2.11.6`](#nats2116)
-	[`nats:2.11.6-alpine`](#nats2116-alpine)
-	[`nats:2.11.6-alpine3.22`](#nats2116-alpine322)
-	[`nats:2.11.6-linux`](#nats2116-linux)
-	[`nats:2.11.6-nanoserver`](#nats2116-nanoserver)
-	[`nats:2.11.6-nanoserver-ltsc2022`](#nats2116-nanoserver-ltsc2022)
-	[`nats:2.11.6-scratch`](#nats2116-scratch)
-	[`nats:2.11.6-windowsservercore`](#nats2116-windowsservercore)
-	[`nats:2.11.6-windowsservercore-ltsc2022`](#nats2116-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:47710a58674c152355730c69fc89d5a86369e3d6d1329cc91767650ce8e0dde6
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
	-	windows version 10.0.20348.3807; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:d01fc7956bcde73411ae93b65ce5f0416787873edc18c6ab3490b1df02ce8802
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
$ docker pull nats@sha256:3fa9fb2909a6d5fc3d03311c4eab7ef44d9d3b07d3060dc3ee09af31615177bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c303eb1d766fef145d081a6efe6667caecdc3d29274580e7cab2c86b555054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2d7c33042de7a2721cc7037921866dd5fd1aef06251cb3b52b803e099650f`  
		Last Modified: Thu, 26 Jun 2025 20:17:43 GMT  
		Size: 6.8 MB (6788052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23999ece2fd82b549915d209c1220df0e2118a8ba5002f08029344c1b4c11b0`  
		Last Modified: Thu, 26 Jun 2025 20:17:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473fef627e81d8cb609092fc5c8cf8b1c63b551ea1b7efabc4ada599bf6b93f3`  
		Last Modified: Thu, 26 Jun 2025 20:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2d087fb959da797f20ae030821cfc23d2ad4a64a60d6366c00c3f8688177c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415bcb886edb909afed1be06569934e7e858ecf295a54aeae89dc46df442b4e`

```dockerfile
```

-	Layers:
	-	`sha256:26b50ad7dfc22e733e46076788aac20cdb3cb8016ce575e3c885503970de2efe`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c407538f141e101cffc6e93ccea6056debe88221abe2666fcea1e76e978812b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10006784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fa8e3a02d934ff0b1507d42fb94e003f944d9c99c410ca998b4f326cb18384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370714c9df343e678c36a394cbc10501b516beab6c5fce69b58b9bebf4249a9f`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 6.5 MB (6504885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126d04e62112930571ace072c0e66e0b6675f7baa4361daebdcc841a347d84c`  
		Last Modified: Thu, 26 Jun 2025 20:17:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8f8539d59dec90772e674c4b9d02b82a9a630df9678a144bcdf9b36bfa563`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:110e8fc0265af245af68f4f13c82bbd22b526e04b3efed7ac6b206d8544346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7a4b99bc73e5fed3010341026e1d528fbf8f910430925d5aefad24bd4df24`

```dockerfile
```

-	Layers:
	-	`sha256:63caa9adf894da2e6e7743936db5d2d122c600e87b80f1315f63e09ce065c928`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:6beb24b9c5ebaf82aa943605e27bf9cc476073c8ba8a85cf1280e7f903933f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9713025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136c6734a14713ef2df657e7b0afeebc4cac53bb1534f54ef1aaf65d1496933c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b94f9506f9f064db25cf04c1de8c94a0f38399389559a320a9bd4bc11f36e7`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 6.5 MB (6492872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158ea2e3a8384adabb2841e2c82603996443c7dc1a808409ac833bbb51029bb`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e59c609640e45233cbb6721667b61baf5f41cff04c3aff825f166c256bee8`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:70765a6f52b790a1246aa15f97c5d982ac1713fa15c251166982d64ec0a5105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52f6b5f6952440758f161a0c7d3b81e299eb2dc579e6179005f62cec504fd4`

```dockerfile
```

-	Layers:
	-	`sha256:5cd3d0a59672dc8da2c92f06824e2b3654d7aeabd529807d6ecf94d9359b5b74`  
		Last Modified: Thu, 26 Jun 2025 23:56:52 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:12f12a82b812d423ae207b4141ff201258813ec9f30a193037818728c969566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10418482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374b467684dc7a7db213ff191ce7d1f2a1545e87c1ebaa2be4aaff0ba71a099`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75474851f507bad54fde1240afe8e8675cd3e4efc177feaebfd6827dc03b482`  
		Last Modified: Thu, 26 Jun 2025 20:17:20 GMT  
		Size: 6.3 MB (6281567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e96f64006c69ac5cd0996766a85be50bc52bda9d77638f9945484be8249ca7`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c3b4a2c9816edaebe425e51b5e596ed27ce69bbe5dce0089042c23add9303`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5bcd0e65eb6744edfa21188c85939ea1d7cda6f477a5bbaeeaacf9a38f1ff062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0c482c58bc50b5774f0872abe58b788bda3f26499322cbd7f38a109b0f0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f51693de89b45487e48ff77661b758d94f3f9e18c237c375453017a1231744c2`  
		Last Modified: Thu, 26 Jun 2025 23:56:55 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:ddd473e4e868ef144ab2d5f9abcf42c5aceb876bb300e0462eebdce5b5f4365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9993129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3072336f828630ea7d0a85fddecbc6eabebebd8559b6776f8c147644cd82c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159dad19c10b3c7682120f345b7e0bea109f9dc391d3a6298d08bb73333d0d59`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 6.3 MB (6261972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7da33fc1b61ecaa43d6f5263a61080be1abe619a070602456f19bceb387f9`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bf6ec9ca48ef6c50947528477f4c16fe8962572e753fa9eedf239e7a401d6`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1e62dcb2bca95114e545acb0e8eff4519f82ce2c57e19687417b288fdbba243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b3c37868ee7b203fddfa4880a0d115e7eb39dec597e967526e3e5fb7a1c4b`

```dockerfile
```

-	Layers:
	-	`sha256:6350f0107c438cca60d4c50ae102aa1fe39670abe71ee66abb23ef856a39ff57`  
		Last Modified: Thu, 26 Jun 2025 23:56:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:676fffad9a719885389d89b25e2658f6b2ffa7ebf49d017b66ae4a959ebd289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6813d2b43b6ca6d4ac54bbb01882cc4ba4237439563dab91499d3ffaf82f9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a12b839b5ac673697b1e2b1c5a3d8e70bc89003735107be2f7098d9a78cea3`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 6.6 MB (6627459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76d719b63c12d9d553830608ff5b6d62b6b8850a3c833d5f108a4e723e1b92`  
		Last Modified: Thu, 26 Jun 2025 20:18:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f6461fda1985f859fa469248cbde00cb5b9a94c750d36727a4fa2fa821f14`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bdcd1a152276665c728f50c64b1ccd43dbdfa0f1532f221e6b409ba7bdb4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f9b5a91c52b3b977a6297761fe63e35ca66d3a969f7d123ac4f67e5dcd7fe`

```dockerfile
```

-	Layers:
	-	`sha256:a25179590d118b79e69af92d0c626fdfe45bf30c8a60c73d2c9e29dcb0f145e0`  
		Last Modified: Thu, 26 Jun 2025 23:57:01 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:d01fc7956bcde73411ae93b65ce5f0416787873edc18c6ab3490b1df02ce8802
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
$ docker pull nats@sha256:3fa9fb2909a6d5fc3d03311c4eab7ef44d9d3b07d3060dc3ee09af31615177bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c303eb1d766fef145d081a6efe6667caecdc3d29274580e7cab2c86b555054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2d7c33042de7a2721cc7037921866dd5fd1aef06251cb3b52b803e099650f`  
		Last Modified: Thu, 26 Jun 2025 20:17:43 GMT  
		Size: 6.8 MB (6788052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23999ece2fd82b549915d209c1220df0e2118a8ba5002f08029344c1b4c11b0`  
		Last Modified: Thu, 26 Jun 2025 20:17:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473fef627e81d8cb609092fc5c8cf8b1c63b551ea1b7efabc4ada599bf6b93f3`  
		Last Modified: Thu, 26 Jun 2025 20:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2d087fb959da797f20ae030821cfc23d2ad4a64a60d6366c00c3f8688177c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415bcb886edb909afed1be06569934e7e858ecf295a54aeae89dc46df442b4e`

```dockerfile
```

-	Layers:
	-	`sha256:26b50ad7dfc22e733e46076788aac20cdb3cb8016ce575e3c885503970de2efe`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c407538f141e101cffc6e93ccea6056debe88221abe2666fcea1e76e978812b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10006784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fa8e3a02d934ff0b1507d42fb94e003f944d9c99c410ca998b4f326cb18384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370714c9df343e678c36a394cbc10501b516beab6c5fce69b58b9bebf4249a9f`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 6.5 MB (6504885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126d04e62112930571ace072c0e66e0b6675f7baa4361daebdcc841a347d84c`  
		Last Modified: Thu, 26 Jun 2025 20:17:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8f8539d59dec90772e674c4b9d02b82a9a630df9678a144bcdf9b36bfa563`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:110e8fc0265af245af68f4f13c82bbd22b526e04b3efed7ac6b206d8544346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7a4b99bc73e5fed3010341026e1d528fbf8f910430925d5aefad24bd4df24`

```dockerfile
```

-	Layers:
	-	`sha256:63caa9adf894da2e6e7743936db5d2d122c600e87b80f1315f63e09ce065c928`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:6beb24b9c5ebaf82aa943605e27bf9cc476073c8ba8a85cf1280e7f903933f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9713025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136c6734a14713ef2df657e7b0afeebc4cac53bb1534f54ef1aaf65d1496933c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b94f9506f9f064db25cf04c1de8c94a0f38399389559a320a9bd4bc11f36e7`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 6.5 MB (6492872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158ea2e3a8384adabb2841e2c82603996443c7dc1a808409ac833bbb51029bb`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e59c609640e45233cbb6721667b61baf5f41cff04c3aff825f166c256bee8`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:70765a6f52b790a1246aa15f97c5d982ac1713fa15c251166982d64ec0a5105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52f6b5f6952440758f161a0c7d3b81e299eb2dc579e6179005f62cec504fd4`

```dockerfile
```

-	Layers:
	-	`sha256:5cd3d0a59672dc8da2c92f06824e2b3654d7aeabd529807d6ecf94d9359b5b74`  
		Last Modified: Thu, 26 Jun 2025 23:56:52 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:12f12a82b812d423ae207b4141ff201258813ec9f30a193037818728c969566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10418482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374b467684dc7a7db213ff191ce7d1f2a1545e87c1ebaa2be4aaff0ba71a099`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75474851f507bad54fde1240afe8e8675cd3e4efc177feaebfd6827dc03b482`  
		Last Modified: Thu, 26 Jun 2025 20:17:20 GMT  
		Size: 6.3 MB (6281567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e96f64006c69ac5cd0996766a85be50bc52bda9d77638f9945484be8249ca7`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c3b4a2c9816edaebe425e51b5e596ed27ce69bbe5dce0089042c23add9303`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5bcd0e65eb6744edfa21188c85939ea1d7cda6f477a5bbaeeaacf9a38f1ff062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0c482c58bc50b5774f0872abe58b788bda3f26499322cbd7f38a109b0f0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f51693de89b45487e48ff77661b758d94f3f9e18c237c375453017a1231744c2`  
		Last Modified: Thu, 26 Jun 2025 23:56:55 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ddd473e4e868ef144ab2d5f9abcf42c5aceb876bb300e0462eebdce5b5f4365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9993129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3072336f828630ea7d0a85fddecbc6eabebebd8559b6776f8c147644cd82c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159dad19c10b3c7682120f345b7e0bea109f9dc391d3a6298d08bb73333d0d59`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 6.3 MB (6261972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7da33fc1b61ecaa43d6f5263a61080be1abe619a070602456f19bceb387f9`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bf6ec9ca48ef6c50947528477f4c16fe8962572e753fa9eedf239e7a401d6`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1e62dcb2bca95114e545acb0e8eff4519f82ce2c57e19687417b288fdbba243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b3c37868ee7b203fddfa4880a0d115e7eb39dec597e967526e3e5fb7a1c4b`

```dockerfile
```

-	Layers:
	-	`sha256:6350f0107c438cca60d4c50ae102aa1fe39670abe71ee66abb23ef856a39ff57`  
		Last Modified: Thu, 26 Jun 2025 23:56:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:676fffad9a719885389d89b25e2658f6b2ffa7ebf49d017b66ae4a959ebd289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6813d2b43b6ca6d4ac54bbb01882cc4ba4237439563dab91499d3ffaf82f9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a12b839b5ac673697b1e2b1c5a3d8e70bc89003735107be2f7098d9a78cea3`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 6.6 MB (6627459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76d719b63c12d9d553830608ff5b6d62b6b8850a3c833d5f108a4e723e1b92`  
		Last Modified: Thu, 26 Jun 2025 20:18:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f6461fda1985f859fa469248cbde00cb5b9a94c750d36727a4fa2fa821f14`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bdcd1a152276665c728f50c64b1ccd43dbdfa0f1532f221e6b409ba7bdb4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f9b5a91c52b3b977a6297761fe63e35ca66d3a969f7d123ac4f67e5dcd7fe`

```dockerfile
```

-	Layers:
	-	`sha256:a25179590d118b79e69af92d0c626fdfe45bf30c8a60c73d2c9e29dcb0f145e0`  
		Last Modified: Thu, 26 Jun 2025 23:57:01 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:a1f720e8485fc0754df5e29fbe72679bcab8bd4234fd92de23ee6bda4a7338e1
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
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:168bb09c4a054a7dec1b1edccdbdc524f9edd8fcec70d4a1cdc9d2201e9c44db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:168bb09c4a054a7dec1b1edccdbdc524f9edd8fcec70d4a1cdc9d2201e9c44db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:a1f720e8485fc0754df5e29fbe72679bcab8bd4234fd92de23ee6bda4a7338e1
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
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:ba84c77cfa19323fd377034bb18a360dc69318846089272b1ea586b7d8101aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:b33dad99cd236d1e37cc4eb8ed9206b6316eda4c64187adc7f1e65ffce3cdb72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287473702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3e602d1e1e318a7bbb885b4a46c7d27f44a285183c5babf5d78687759b53`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 20:17:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.5/nats-server-v2.11.5-windows-amd64.zip
# Thu, 26 Jun 2025 20:17:15 GMT
ENV NATS_SERVER_SHASUM=32b71f33c65cbee21894a2a7b82e5e8f0d7b15071ed591a115637ae9bbf67fc5
# Thu, 26 Jun 2025 20:17:32 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Jun 2025 20:17:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Jun 2025 20:17:53 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 20:17:54 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 20:17:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 20:17:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1c92883cf6e9b17042332de88a3dc30e79476a8df292435d274ff25663a63`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363721f0db417ab1ab377e6bf9123acf262a0b35c2c361e1026c89439c93c089`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5558cc62efdd7b0998e08a4ecfa776ef70871516275984b80a192f2c15ac5b5a`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa5c078273d6cf527c751ed1c752110b3a862d0f746ef91c23feea7ca14353`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b2cfcd8172bc275be5a4eef1b7fb8b868b5c35c2ae018f62cd580e0a9ec74c`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e632d9a39cdd638851c72936a39eebbcf700962d71ce0fce0ab1a6463fcd76`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 352.0 KB (352026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcaa6c58043c1e708d7ebe440178de6af7dd752846fe9dadaf8e69dc67357c`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 6.9 MB (6857935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba4e672ef32c33580896edc49992582d020ca5ee032917311bf0eb466dfde1`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74212ea9e5dfddac2be0bf465d397594828dd1c10415d6c523b647fa3738834`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb92634ba25710d95df0eec641298bc77fbb7eab9879e0681faf82f0e6aa2d8`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecdd379742fa5e86e868683db8922cc7e21ff8a9d87e7e55eec7c3277575a77`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ba84c77cfa19323fd377034bb18a360dc69318846089272b1ea586b7d8101aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:b33dad99cd236d1e37cc4eb8ed9206b6316eda4c64187adc7f1e65ffce3cdb72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287473702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3e602d1e1e318a7bbb885b4a46c7d27f44a285183c5babf5d78687759b53`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 20:17:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.5/nats-server-v2.11.5-windows-amd64.zip
# Thu, 26 Jun 2025 20:17:15 GMT
ENV NATS_SERVER_SHASUM=32b71f33c65cbee21894a2a7b82e5e8f0d7b15071ed591a115637ae9bbf67fc5
# Thu, 26 Jun 2025 20:17:32 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Jun 2025 20:17:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Jun 2025 20:17:53 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 20:17:54 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 20:17:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 20:17:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1c92883cf6e9b17042332de88a3dc30e79476a8df292435d274ff25663a63`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363721f0db417ab1ab377e6bf9123acf262a0b35c2c361e1026c89439c93c089`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5558cc62efdd7b0998e08a4ecfa776ef70871516275984b80a192f2c15ac5b5a`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa5c078273d6cf527c751ed1c752110b3a862d0f746ef91c23feea7ca14353`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b2cfcd8172bc275be5a4eef1b7fb8b868b5c35c2ae018f62cd580e0a9ec74c`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e632d9a39cdd638851c72936a39eebbcf700962d71ce0fce0ab1a6463fcd76`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 352.0 KB (352026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcaa6c58043c1e708d7ebe440178de6af7dd752846fe9dadaf8e69dc67357c`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 6.9 MB (6857935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba4e672ef32c33580896edc49992582d020ca5ee032917311bf0eb466dfde1`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74212ea9e5dfddac2be0bf465d397594828dd1c10415d6c523b647fa3738834`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb92634ba25710d95df0eec641298bc77fbb7eab9879e0681faf82f0e6aa2d8`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecdd379742fa5e86e868683db8922cc7e21ff8a9d87e7e55eec7c3277575a77`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:9eabc00ace045e4c7eb054e512ec9fe8298e80f6e833dc6a5bace5751f2b60a0
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
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:f65d9011e91978762873b60bad589dd1d069892de58c59a77f99fa23d4e241ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128844428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f59f0a1ad2865b23cf2fc76e3c192a8cb391a545c47eddab89fcb59e856c972`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:18:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 22:18:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 22:18:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 22:18:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d943e1ddb56fdcd2d93bf87b1cbbe2261f920227e2d768f360a8222f136be`  
		Last Modified: Tue, 10 Jun 2025 22:19:23 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a778f078cc1dc51413861c198bd4ffc975a508f6945cda0618fe65133f6dc`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 6.3 MB (6298057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cf601e462dce927a2870745f7e860e5fe7b77cad04128eaee59e8199660cd0`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08974ac79b0af496dccd4a8f8536ae50791cc5dccf7234e3550f0b529e4d1924`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e6edffc2cac847713e2b2c563f19f04cb886bd663424f4bceff8065529ed58`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae12d415a55085b58b94f06bfadd817f4b787c0d2c023cdfaacdcac53cd56c`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.22`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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

### `nats:2.10-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:8c79c1f54f6d01c4041c23a9a3b8c15b064f29af3aa88dfb3d0f51fbb49bd966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:f65d9011e91978762873b60bad589dd1d069892de58c59a77f99fa23d4e241ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128844428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f59f0a1ad2865b23cf2fc76e3c192a8cb391a545c47eddab89fcb59e856c972`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:18:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 22:18:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 22:18:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 22:18:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d943e1ddb56fdcd2d93bf87b1cbbe2261f920227e2d768f360a8222f136be`  
		Last Modified: Tue, 10 Jun 2025 22:19:23 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a778f078cc1dc51413861c198bd4ffc975a508f6945cda0618fe65133f6dc`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 6.3 MB (6298057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cf601e462dce927a2870745f7e860e5fe7b77cad04128eaee59e8199660cd0`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08974ac79b0af496dccd4a8f8536ae50791cc5dccf7234e3550f0b529e4d1924`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e6edffc2cac847713e2b2c563f19f04cb886bd663424f4bceff8065529ed58`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae12d415a55085b58b94f06bfadd817f4b787c0d2c023cdfaacdcac53cd56c`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:8c79c1f54f6d01c4041c23a9a3b8c15b064f29af3aa88dfb3d0f51fbb49bd966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:f65d9011e91978762873b60bad589dd1d069892de58c59a77f99fa23d4e241ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128844428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f59f0a1ad2865b23cf2fc76e3c192a8cb391a545c47eddab89fcb59e856c972`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:18:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 22:18:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 22:18:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 22:18:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d943e1ddb56fdcd2d93bf87b1cbbe2261f920227e2d768f360a8222f136be`  
		Last Modified: Tue, 10 Jun 2025 22:19:23 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a778f078cc1dc51413861c198bd4ffc975a508f6945cda0618fe65133f6dc`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 6.3 MB (6298057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cf601e462dce927a2870745f7e860e5fe7b77cad04128eaee59e8199660cd0`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08974ac79b0af496dccd4a8f8536ae50791cc5dccf7234e3550f0b529e4d1924`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e6edffc2cac847713e2b2c563f19f04cb886bd663424f4bceff8065529ed58`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae12d415a55085b58b94f06bfadd817f4b787c0d2c023cdfaacdcac53cd56c`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:0ab3c8ee66b15a4b147c04e3f4301aac1334ebf6a70d4b07a93679af8d34c254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:a25052dd5249a4ac9c6e9c4ae194d52a9979781c5ae36a09b0cced5200c298f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287260906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb576d528ae459c09658e6e949328a4c98516b4391ce44f6bff2bf053b14253`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:25:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:25:56 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 21:25:57 GMT
ENV NATS_SERVER=2.10.29
# Tue, 10 Jun 2025 21:25:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 10 Jun 2025 21:25:59 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 10 Jun 2025 21:26:06 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Jun 2025 21:26:23 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Jun 2025 21:26:23 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 21:26:24 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 21:26:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 21:26:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03fa6e8dcebd10cbabd71849abba90d8230a6d47405d711bab12e35203a63b9`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121141b475f524a98ee7e4af4b1274e28f03d3bc090c4e1b55a98a84486a8309`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a8eb095f3e2c3a2e3f1318ced354c98318b61457e1d6ba434ea3654cbde72`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2206b0c472f1b0c85c9b94a81704bf41c6cfeafd9e915b95a490c2109738b2ee`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250a330061e872e115ff85ff7461e4f92aa3e9ed516b7e432082aa34642b290`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8572dd98ea0ef61a0843821b36aac3e58041a2be8071dd25665e5fa3590527`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 348.6 KB (348551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6062377e4c4fe3d7531032cc2df686ab2d613904e56f6ef9bc60b9cf4f2441ef`  
		Last Modified: Tue, 10 Jun 2025 21:28:08 GMT  
		Size: 6.6 MB (6648625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec6eed39877a5460de51b98c56a7e7d509ec4aabfb2ed9afc66e96b6f18b95f`  
		Last Modified: Tue, 10 Jun 2025 22:08:43 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f005d0d4060b115a4d79dc95f9ee4c786a3e34d9a990bd9df7341724f7e2db66`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648190fece04bf0b13646b71ed1f6b029b57548a5e1ac1f1b7a4a001998a5fc7`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5620414082da2252b6bd2be3eb31ecab929d89e43049e8e9b6c91e136526c39`  
		Last Modified: Tue, 10 Jun 2025 22:08:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:0ab3c8ee66b15a4b147c04e3f4301aac1334ebf6a70d4b07a93679af8d34c254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:a25052dd5249a4ac9c6e9c4ae194d52a9979781c5ae36a09b0cced5200c298f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287260906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb576d528ae459c09658e6e949328a4c98516b4391ce44f6bff2bf053b14253`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:25:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:25:56 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 21:25:57 GMT
ENV NATS_SERVER=2.10.29
# Tue, 10 Jun 2025 21:25:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 10 Jun 2025 21:25:59 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 10 Jun 2025 21:26:06 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Jun 2025 21:26:23 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Jun 2025 21:26:23 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 21:26:24 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 21:26:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 21:26:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03fa6e8dcebd10cbabd71849abba90d8230a6d47405d711bab12e35203a63b9`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121141b475f524a98ee7e4af4b1274e28f03d3bc090c4e1b55a98a84486a8309`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a8eb095f3e2c3a2e3f1318ced354c98318b61457e1d6ba434ea3654cbde72`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2206b0c472f1b0c85c9b94a81704bf41c6cfeafd9e915b95a490c2109738b2ee`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250a330061e872e115ff85ff7461e4f92aa3e9ed516b7e432082aa34642b290`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8572dd98ea0ef61a0843821b36aac3e58041a2be8071dd25665e5fa3590527`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 348.6 KB (348551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6062377e4c4fe3d7531032cc2df686ab2d613904e56f6ef9bc60b9cf4f2441ef`  
		Last Modified: Tue, 10 Jun 2025 21:28:08 GMT  
		Size: 6.6 MB (6648625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec6eed39877a5460de51b98c56a7e7d509ec4aabfb2ed9afc66e96b6f18b95f`  
		Last Modified: Tue, 10 Jun 2025 22:08:43 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f005d0d4060b115a4d79dc95f9ee4c786a3e34d9a990bd9df7341724f7e2db66`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648190fece04bf0b13646b71ed1f6b029b57548a5e1ac1f1b7a4a001998a5fc7`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5620414082da2252b6bd2be3eb31ecab929d89e43049e8e9b6c91e136526c39`  
		Last Modified: Tue, 10 Jun 2025 22:08:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29`

```console
$ docker pull nats@sha256:9eabc00ace045e4c7eb054e512ec9fe8298e80f6e833dc6a5bace5751f2b60a0
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
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10.29` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:f65d9011e91978762873b60bad589dd1d069892de58c59a77f99fa23d4e241ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128844428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f59f0a1ad2865b23cf2fc76e3c192a8cb391a545c47eddab89fcb59e856c972`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:18:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 22:18:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 22:18:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 22:18:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d943e1ddb56fdcd2d93bf87b1cbbe2261f920227e2d768f360a8222f136be`  
		Last Modified: Tue, 10 Jun 2025 22:19:23 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a778f078cc1dc51413861c198bd4ffc975a508f6945cda0618fe65133f6dc`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 6.3 MB (6298057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cf601e462dce927a2870745f7e860e5fe7b77cad04128eaee59e8199660cd0`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08974ac79b0af496dccd4a8f8536ae50791cc5dccf7234e3550f0b529e4d1924`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e6edffc2cac847713e2b2c563f19f04cb886bd663424f4bceff8065529ed58`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae12d415a55085b58b94f06bfadd817f4b787c0d2c023cdfaacdcac53cd56c`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-alpine`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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

### `nats:2.10.29-alpine` - linux; amd64

```console
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-alpine3.22`

```console
$ docker pull nats@sha256:e4ff89435a697d4dc2269f44a9cc03c0ce206bf2ec0c5e86346eec2c793968c1
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

### `nats:2.10.29-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:165f3f9e87763690201921b55fb96b150d36d84642b6f38bb19597e6d7221e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10437622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1758922c6ce2a574c21623a2d02a76150fe7e8e4e2d52fb16edf9fb7e7e4f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c43a19c65dc59aaf516d2615f3588ad1dc1017d49dcb9aa321aeeef4b7ffc1`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 6.6 MB (6639806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:acc886b722ace04957f77e3a1c8e6749940f7041386ce05210e8ea4c69f46932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650a81620e7f82cdb309ecf6157c2da44d151b3566cf6de4864c7dc6d20d683c`

```dockerfile
```

-	Layers:
	-	`sha256:02ec91a27ddca6b7dd03de7acc756b53883df80e809a4ac3e313f849e98fdbc1`  
		Last Modified: Tue, 03 Jun 2025 20:57:34 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:261dc298ca8bb3e809b2fa84c845abe8fc4a133a3a6d81b41d5fa052f2e2d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de804bb490ce73fbc139af75dd82c0b81800c69fecddde21775f3528a6d7c7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562b8a11b8ed69d392bd2d9542980acf48db7b4527ff82479fb7de58d715714`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 6.4 MB (6363844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3005b967f68a27687c38d68520bdede8bff0aaf8a4c45416991973c3ceb4a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727afe280399541b9353f4c6fd9eeb040798b41369e880443022658368b70f8d`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7bc8e0c9bf979f2e1a4b1c68db710249a14826eb638af9a1a90cf60a5860e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605c808048d40222ff44f9f4fab194ef118bc38ba23cdbd2cb00b66d1f4a768`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a85b4eba1b90277a6099a69d60e91db6dbe50ec0761e7e0713eaba4243490`  
		Last Modified: Tue, 03 Jun 2025 20:57:37 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c49785ef72f6851e19acd1effd844500de145fe8f8b60deb80f4b412acfd8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c42fbe838dc45066f11b49b3a2b289f1e68ca79a337e2d37a8c9258a4d69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c60b436ca9be1cafae973b2673faaf38e3c6f55f8bcf1808f09815771e3688d`  
		Last Modified: Tue, 03 Jun 2025 20:58:00 GMT  
		Size: 6.4 MB (6351017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3c878be8ff45a5224d95e5e15f26bbec36e0946930597d58789fb8b90cd85`  
		Last Modified: Tue, 03 Jun 2025 18:02:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde678942fe21a15ddffc4415cc8cdfea1b4ec957fbfddc20b2e769c8f24b887`  
		Last Modified: Tue, 03 Jun 2025 18:02:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0e862f0aa96b7c561038da51377fdd552e6ad618d4148a8abcf19463c287e82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b404fa016eca9854ca662633cbbbed396ffd14707165264453f3887486787cf`

```dockerfile
```

-	Layers:
	-	`sha256:49b59c86b7347c12453d29446f15f08a34553aac5bde9dad6828b2cca678778f`  
		Last Modified: Tue, 03 Jun 2025 20:57:41 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:285a2a4cd223ee5a09948483638d63000a1012062bcecd10558588dcea57af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1915225864493be141ed87c713508d93dc744b32d85e0c549444133809ac37a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988a5cc26a525b12202b4ede8dbadf7282232fa3202588c82228cc51312a2db`  
		Last Modified: Tue, 03 Jun 2025 18:12:34 GMT  
		Size: 6.1 MB (6145683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed6725710b37dc92dbdc9beb40eddc4b06a58b847403c608550796d72c7430`  
		Last Modified: Tue, 03 Jun 2025 18:12:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3e1af6617ced1a84b929dfa36cc1aeefede7065ee2c580030f864336d30215`  
		Last Modified: Tue, 03 Jun 2025 18:12:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b58de4f1cc2ff62b12af617c5814335385fc4252143980d31ec8b385b8a0281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429f6e62c50bb7cc5184af5e6f318d09a3ca04b31430f71f3d35eaf9c080d52`

```dockerfile
```

-	Layers:
	-	`sha256:be4126cc80da8c7edb98f1b5a8da59348d702f75d87e8375559dbcaa9e628273`  
		Last Modified: Tue, 03 Jun 2025 20:57:45 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9c85f40d23ab0ee0d9ae30d532b565f8a86573f0300420151060cbedcef5e8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c32a0cc3e550a3e68b0856e8da573eacf0ab169da68dbdccf9b2689d5820d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4574fc8f9c31a7e7c3096b2295a13bb991034e66aaee26f0c8bb92f4965f89`  
		Last Modified: Tue, 03 Jun 2025 18:15:03 GMT  
		Size: 6.1 MB (6125536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26043e6e9cf09cbd98c4343bed49c94ad7825b33e6dc73d6aef9f860bca1f5f7`  
		Last Modified: Tue, 03 Jun 2025 18:11:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d10afb72d6f0cf76c7bb3528287bc589928122df027b23f8226d7c2926290`  
		Last Modified: Tue, 03 Jun 2025 18:11:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:946551fed6e10788bcccc2dddf5722a62178223fd200dd771430b848fdb40f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5564c58fcb5f6b52983f1f0b07658184fab57abaf366dfe4756655fff3c9c166`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4252ac8a827db1eaae604fe622384be59f71e498988ad120c735b8870df72`  
		Last Modified: Tue, 03 Jun 2025 20:57:48 GMT  
		Size: 13.2 KB (13165 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:9b4247153f56677441a4087e2f007d554133f2b656c8e24c4e7f283e13775ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10131011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e1ab87078f53cf2d3de1cc3d84ffcb8a89160be9e97291e74e906c3f21208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.10.29
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeaa39221515ea4113a7177048180cf406a52328259a52ab2741589dbd942be`  
		Last Modified: Tue, 03 Jun 2025 18:09:14 GMT  
		Size: 6.5 MB (6482513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877186488f8186bc3fd5f22ae5055586ca7ba35d22bd8b44e183d8de602b7a86`  
		Last Modified: Tue, 03 Jun 2025 18:03:59 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d673d1efb6b2752e2fcace714fb45f3efb76e03432446c01c5926e0defc8dd`  
		Last Modified: Tue, 03 Jun 2025 18:04:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8271d38fc2c1db1251228a13e31422f50095cebc22fa791967b817d9fab8d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbbb56c5affc65c809913f0c2e71df3151bb57a4f1ec03a70ef0f217a8bc3f8`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a134b43959c10be25f3307dfd04c7c345280c8d0f92932ddf07e454304b3b`  
		Last Modified: Tue, 03 Jun 2025 20:57:52 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-linux`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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

### `nats:2.10.29-linux` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-nanoserver`

```console
$ docker pull nats@sha256:8c79c1f54f6d01c4041c23a9a3b8c15b064f29af3aa88dfb3d0f51fbb49bd966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10.29-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:f65d9011e91978762873b60bad589dd1d069892de58c59a77f99fa23d4e241ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128844428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f59f0a1ad2865b23cf2fc76e3c192a8cb391a545c47eddab89fcb59e856c972`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:18:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 22:18:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 22:18:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 22:18:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d943e1ddb56fdcd2d93bf87b1cbbe2261f920227e2d768f360a8222f136be`  
		Last Modified: Tue, 10 Jun 2025 22:19:23 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a778f078cc1dc51413861c198bd4ffc975a508f6945cda0618fe65133f6dc`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 6.3 MB (6298057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cf601e462dce927a2870745f7e860e5fe7b77cad04128eaee59e8199660cd0`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08974ac79b0af496dccd4a8f8536ae50791cc5dccf7234e3550f0b529e4d1924`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e6edffc2cac847713e2b2c563f19f04cb886bd663424f4bceff8065529ed58`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae12d415a55085b58b94f06bfadd817f4b787c0d2c023cdfaacdcac53cd56c`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:8c79c1f54f6d01c4041c23a9a3b8c15b064f29af3aa88dfb3d0f51fbb49bd966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10.29-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:f65d9011e91978762873b60bad589dd1d069892de58c59a77f99fa23d4e241ac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128844428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f59f0a1ad2865b23cf2fc76e3c192a8cb391a545c47eddab89fcb59e856c972`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:18:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 10 Jun 2025 22:18:53 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 22:18:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 22:18:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 22:18:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d943e1ddb56fdcd2d93bf87b1cbbe2261f920227e2d768f360a8222f136be`  
		Last Modified: Tue, 10 Jun 2025 22:19:23 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a778f078cc1dc51413861c198bd4ffc975a508f6945cda0618fe65133f6dc`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 6.3 MB (6298057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cf601e462dce927a2870745f7e860e5fe7b77cad04128eaee59e8199660cd0`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08974ac79b0af496dccd4a8f8536ae50791cc5dccf7234e3550f0b529e4d1924`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e6edffc2cac847713e2b2c563f19f04cb886bd663424f4bceff8065529ed58`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae12d415a55085b58b94f06bfadd817f4b787c0d2c023cdfaacdcac53cd56c`  
		Last Modified: Tue, 10 Jun 2025 22:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-scratch`

```console
$ docker pull nats@sha256:28edd413f190fb139ed600359da94e5a583e999dce2750488c75bef692250817
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

### `nats:2.10.29-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f030f79672be88d009b75f61c2cb5fe9d07ad3364742a9b27cd60c9338ffafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4962b82a0ae69663e5a74740285899ca5957c69f6c53bf82311476aa1fae5ef8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbf4b75f5de6580e5f213d7ab14b95f53d66cad454497b06e46c4a440b502d6`  
		Last Modified: Tue, 03 Jun 2025 18:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5edca7674c56d6da9be7a373f78942e4c4aa5f175636ee35ccffba1533772e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3176d2028656537e4bfe7efebe9f8fcc985778a684370b2eff8c909b50c6f3`

```dockerfile
```

-	Layers:
	-	`sha256:5f2aca3d9450c14453dcb34e8c6b2a5a9a11673e6f7baeb3c28b7b435f2789d0`  
		Last Modified: Tue, 03 Jun 2025 20:57:19 GMT  
		Size: 8.7 KB (8710 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7a72209661fa798f94ca59fe982425636af6df596e83cc2bdb1b1ebde04a57c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09f5ba25ee4d10359cc31039d1a9a05f150b96f797eb6ca7d155076fd547bb9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb3048cc57f790e44bb317519f7d61ce9e2d2cdcd7a57ac04cdf293bdd74a`  
		Last Modified: Tue, 03 Jun 2025 18:08:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9c3d54e7088aa0eb163c2eeb032e0d168126cdf0af77576fdc60ea726a70e690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8e6de48fcf449ba2519083b4bc5415c135d29db13e6c6b49b06eb5c5b766a1`

```dockerfile
```

-	Layers:
	-	`sha256:224e3a5982d8875c00e7bc85a73e0963da1394057839ae2fc9902d645dfd92ac`  
		Last Modified: Tue, 03 Jun 2025 20:57:22 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:0e599020477e9ff23b27b1865ecb60543ed1535464abc4e188798db623bf31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93191df559a8ac9ecaf2375c3c0650313c7cf85b7a5c1828496f963214a3b7a8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe6cace6dcb5e8d0b30a41e65b06eac2b2db46153d20610970774ad0c6ae658`  
		Last Modified: Tue, 03 Jun 2025 18:08:02 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:20322b26c9067df443a4c1d508864fa6c56d75e95c6f7b54af8aa64244c36523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f876797d7587f086738701ffc4137685187baf0e93a73bec7ca91ab37de8e2`

```dockerfile
```

-	Layers:
	-	`sha256:beb15a763ca188b107db77465e3fbd30750125d1abfcb5ce92acbb109fac9e12`  
		Last Modified: Tue, 03 Jun 2025 20:57:26 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:032295d595a30a6e02710d95f3b3371b26f67558194ac6e026d302bda83f82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2122a29fe765e930ef544b90d5626a1b68d149b8d8e01d11af499a44ad680e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebcf7fe8e5b3a56dc480f7baa83adbd38d2bbed924d023380166bd9981fd69`  
		Last Modified: Tue, 03 Jun 2025 18:23:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f18a5550f0cb7923ac9d1d849700acba1c8edb7aae430b47bab129cbd920c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d59fba1c4b597d8c4c1f24f141dd0eb7e85a15f0bef993397327c84bc7dbc29`

```dockerfile
```

-	Layers:
	-	`sha256:b2f945ed0151cbf2eb4c531a81285a4227388550be1b38523fe42a95a739afba`  
		Last Modified: Tue, 03 Jun 2025 20:57:30 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:a1ee7f0765400218d94bcf05b108750a2c1d828a1ddc229520f68cd1a729772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce2215357ad2fb81086a7d81d51e879117d3d8e82b33a5594ad71cb42c9bd91`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba77e33529d308f759dde5ea0c2bc855d0fe710addc9b1ea041e795164831318`  
		Last Modified: Tue, 03 Jun 2025 18:22:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:458018497dd1f52d267442fa606155e76006f16995d106b8de40fab5ce15d07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e4beb2fa95e1452e4c3038fa80d0473aa25a3f0889c913e70dd71ab4adf9b4`

```dockerfile
```

-	Layers:
	-	`sha256:ab157204d16e4104829c5bb33652543a9248eea5ff2da1aa7f73be9a05e080d7`  
		Last Modified: Tue, 03 Jun 2025 20:57:33 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d6cee6070c0808acf67782ea629ef2b095b877a064ef586239ad9d751fede448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5b2af2bb2f493ce23801f42d46661f10316f40ccd8f2c5fa91526f391f8845`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Jun 2025 16:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 02 Jun 2025 16:53:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 02 Jun 2025 16:53:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 02 Jun 2025 16:53:31 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Jun 2025 16:53:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63335d678adcf565f57b5c9a5020490b91f64dfcb434b646af92d61010878019`  
		Last Modified: Tue, 03 Jun 2025 18:09:40 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8d414aad040bcc21d6e5781cc4ef29badad9a7a3274a8a253ec0a84575ca6ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecca08806a2ed272df4613365d603a586113ca6a6aea54411b44f1d3b61d05`

```dockerfile
```

-	Layers:
	-	`sha256:d641a2c5f6581536130597650655cb4668997c123bb18fbf12c0cdab75476fac`  
		Last Modified: Tue, 03 Jun 2025 20:57:38 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-windowsservercore`

```console
$ docker pull nats@sha256:0ab3c8ee66b15a4b147c04e3f4301aac1334ebf6a70d4b07a93679af8d34c254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10.29-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:a25052dd5249a4ac9c6e9c4ae194d52a9979781c5ae36a09b0cced5200c298f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287260906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb576d528ae459c09658e6e949328a4c98516b4391ce44f6bff2bf053b14253`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:25:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:25:56 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 21:25:57 GMT
ENV NATS_SERVER=2.10.29
# Tue, 10 Jun 2025 21:25:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 10 Jun 2025 21:25:59 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 10 Jun 2025 21:26:06 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Jun 2025 21:26:23 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Jun 2025 21:26:23 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 21:26:24 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 21:26:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 21:26:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03fa6e8dcebd10cbabd71849abba90d8230a6d47405d711bab12e35203a63b9`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121141b475f524a98ee7e4af4b1274e28f03d3bc090c4e1b55a98a84486a8309`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a8eb095f3e2c3a2e3f1318ced354c98318b61457e1d6ba434ea3654cbde72`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2206b0c472f1b0c85c9b94a81704bf41c6cfeafd9e915b95a490c2109738b2ee`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250a330061e872e115ff85ff7461e4f92aa3e9ed516b7e432082aa34642b290`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8572dd98ea0ef61a0843821b36aac3e58041a2be8071dd25665e5fa3590527`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 348.6 KB (348551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6062377e4c4fe3d7531032cc2df686ab2d613904e56f6ef9bc60b9cf4f2441ef`  
		Last Modified: Tue, 10 Jun 2025 21:28:08 GMT  
		Size: 6.6 MB (6648625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec6eed39877a5460de51b98c56a7e7d509ec4aabfb2ed9afc66e96b6f18b95f`  
		Last Modified: Tue, 10 Jun 2025 22:08:43 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f005d0d4060b115a4d79dc95f9ee4c786a3e34d9a990bd9df7341724f7e2db66`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648190fece04bf0b13646b71ed1f6b029b57548a5e1ac1f1b7a4a001998a5fc7`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5620414082da2252b6bd2be3eb31ecab929d89e43049e8e9b6c91e136526c39`  
		Last Modified: Tue, 10 Jun 2025 22:08:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:0ab3c8ee66b15a4b147c04e3f4301aac1334ebf6a70d4b07a93679af8d34c254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.10.29-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:a25052dd5249a4ac9c6e9c4ae194d52a9979781c5ae36a09b0cced5200c298f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287260906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb576d528ae459c09658e6e949328a4c98516b4391ce44f6bff2bf053b14253`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:25:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Jun 2025 21:25:56 GMT
ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 21:25:57 GMT
ENV NATS_SERVER=2.10.29
# Tue, 10 Jun 2025 21:25:58 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 10 Jun 2025 21:25:59 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 10 Jun 2025 21:26:06 GMT
RUN Set-PSDebug -Trace 2
# Tue, 10 Jun 2025 21:26:23 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 10 Jun 2025 21:26:23 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 21:26:24 GMT
EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 21:26:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 21:26:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03fa6e8dcebd10cbabd71849abba90d8230a6d47405d711bab12e35203a63b9`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121141b475f524a98ee7e4af4b1274e28f03d3bc090c4e1b55a98a84486a8309`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8a8eb095f3e2c3a2e3f1318ced354c98318b61457e1d6ba434ea3654cbde72`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2206b0c472f1b0c85c9b94a81704bf41c6cfeafd9e915b95a490c2109738b2ee`  
		Last Modified: Tue, 10 Jun 2025 21:28:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c250a330061e872e115ff85ff7461e4f92aa3e9ed516b7e432082aa34642b290`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8572dd98ea0ef61a0843821b36aac3e58041a2be8071dd25665e5fa3590527`  
		Last Modified: Tue, 10 Jun 2025 21:28:07 GMT  
		Size: 348.6 KB (348551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6062377e4c4fe3d7531032cc2df686ab2d613904e56f6ef9bc60b9cf4f2441ef`  
		Last Modified: Tue, 10 Jun 2025 21:28:08 GMT  
		Size: 6.6 MB (6648625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec6eed39877a5460de51b98c56a7e7d509ec4aabfb2ed9afc66e96b6f18b95f`  
		Last Modified: Tue, 10 Jun 2025 22:08:43 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f005d0d4060b115a4d79dc95f9ee4c786a3e34d9a990bd9df7341724f7e2db66`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648190fece04bf0b13646b71ed1f6b029b57548a5e1ac1f1b7a4a001998a5fc7`  
		Last Modified: Tue, 10 Jun 2025 22:08:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5620414082da2252b6bd2be3eb31ecab929d89e43049e8e9b6c91e136526c39`  
		Last Modified: Tue, 10 Jun 2025 22:08:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:47710a58674c152355730c69fc89d5a86369e3d6d1329cc91767650ce8e0dde6
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
	-	windows version 10.0.20348.3807; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:d01fc7956bcde73411ae93b65ce5f0416787873edc18c6ab3490b1df02ce8802
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
$ docker pull nats@sha256:3fa9fb2909a6d5fc3d03311c4eab7ef44d9d3b07d3060dc3ee09af31615177bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c303eb1d766fef145d081a6efe6667caecdc3d29274580e7cab2c86b555054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2d7c33042de7a2721cc7037921866dd5fd1aef06251cb3b52b803e099650f`  
		Last Modified: Thu, 26 Jun 2025 20:17:43 GMT  
		Size: 6.8 MB (6788052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23999ece2fd82b549915d209c1220df0e2118a8ba5002f08029344c1b4c11b0`  
		Last Modified: Thu, 26 Jun 2025 20:17:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473fef627e81d8cb609092fc5c8cf8b1c63b551ea1b7efabc4ada599bf6b93f3`  
		Last Modified: Thu, 26 Jun 2025 20:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2d087fb959da797f20ae030821cfc23d2ad4a64a60d6366c00c3f8688177c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415bcb886edb909afed1be06569934e7e858ecf295a54aeae89dc46df442b4e`

```dockerfile
```

-	Layers:
	-	`sha256:26b50ad7dfc22e733e46076788aac20cdb3cb8016ce575e3c885503970de2efe`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c407538f141e101cffc6e93ccea6056debe88221abe2666fcea1e76e978812b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10006784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fa8e3a02d934ff0b1507d42fb94e003f944d9c99c410ca998b4f326cb18384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370714c9df343e678c36a394cbc10501b516beab6c5fce69b58b9bebf4249a9f`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 6.5 MB (6504885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126d04e62112930571ace072c0e66e0b6675f7baa4361daebdcc841a347d84c`  
		Last Modified: Thu, 26 Jun 2025 20:17:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8f8539d59dec90772e674c4b9d02b82a9a630df9678a144bcdf9b36bfa563`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:110e8fc0265af245af68f4f13c82bbd22b526e04b3efed7ac6b206d8544346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7a4b99bc73e5fed3010341026e1d528fbf8f910430925d5aefad24bd4df24`

```dockerfile
```

-	Layers:
	-	`sha256:63caa9adf894da2e6e7743936db5d2d122c600e87b80f1315f63e09ce065c928`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:6beb24b9c5ebaf82aa943605e27bf9cc476073c8ba8a85cf1280e7f903933f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9713025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136c6734a14713ef2df657e7b0afeebc4cac53bb1534f54ef1aaf65d1496933c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b94f9506f9f064db25cf04c1de8c94a0f38399389559a320a9bd4bc11f36e7`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 6.5 MB (6492872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158ea2e3a8384adabb2841e2c82603996443c7dc1a808409ac833bbb51029bb`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e59c609640e45233cbb6721667b61baf5f41cff04c3aff825f166c256bee8`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:70765a6f52b790a1246aa15f97c5d982ac1713fa15c251166982d64ec0a5105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52f6b5f6952440758f161a0c7d3b81e299eb2dc579e6179005f62cec504fd4`

```dockerfile
```

-	Layers:
	-	`sha256:5cd3d0a59672dc8da2c92f06824e2b3654d7aeabd529807d6ecf94d9359b5b74`  
		Last Modified: Thu, 26 Jun 2025 23:56:52 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:12f12a82b812d423ae207b4141ff201258813ec9f30a193037818728c969566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10418482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374b467684dc7a7db213ff191ce7d1f2a1545e87c1ebaa2be4aaff0ba71a099`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75474851f507bad54fde1240afe8e8675cd3e4efc177feaebfd6827dc03b482`  
		Last Modified: Thu, 26 Jun 2025 20:17:20 GMT  
		Size: 6.3 MB (6281567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e96f64006c69ac5cd0996766a85be50bc52bda9d77638f9945484be8249ca7`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c3b4a2c9816edaebe425e51b5e596ed27ce69bbe5dce0089042c23add9303`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5bcd0e65eb6744edfa21188c85939ea1d7cda6f477a5bbaeeaacf9a38f1ff062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0c482c58bc50b5774f0872abe58b788bda3f26499322cbd7f38a109b0f0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f51693de89b45487e48ff77661b758d94f3f9e18c237c375453017a1231744c2`  
		Last Modified: Thu, 26 Jun 2025 23:56:55 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:ddd473e4e868ef144ab2d5f9abcf42c5aceb876bb300e0462eebdce5b5f4365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9993129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3072336f828630ea7d0a85fddecbc6eabebebd8559b6776f8c147644cd82c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159dad19c10b3c7682120f345b7e0bea109f9dc391d3a6298d08bb73333d0d59`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 6.3 MB (6261972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7da33fc1b61ecaa43d6f5263a61080be1abe619a070602456f19bceb387f9`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bf6ec9ca48ef6c50947528477f4c16fe8962572e753fa9eedf239e7a401d6`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1e62dcb2bca95114e545acb0e8eff4519f82ce2c57e19687417b288fdbba243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b3c37868ee7b203fddfa4880a0d115e7eb39dec597e967526e3e5fb7a1c4b`

```dockerfile
```

-	Layers:
	-	`sha256:6350f0107c438cca60d4c50ae102aa1fe39670abe71ee66abb23ef856a39ff57`  
		Last Modified: Thu, 26 Jun 2025 23:56:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:676fffad9a719885389d89b25e2658f6b2ffa7ebf49d017b66ae4a959ebd289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6813d2b43b6ca6d4ac54bbb01882cc4ba4237439563dab91499d3ffaf82f9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a12b839b5ac673697b1e2b1c5a3d8e70bc89003735107be2f7098d9a78cea3`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 6.6 MB (6627459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76d719b63c12d9d553830608ff5b6d62b6b8850a3c833d5f108a4e723e1b92`  
		Last Modified: Thu, 26 Jun 2025 20:18:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f6461fda1985f859fa469248cbde00cb5b9a94c750d36727a4fa2fa821f14`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bdcd1a152276665c728f50c64b1ccd43dbdfa0f1532f221e6b409ba7bdb4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f9b5a91c52b3b977a6297761fe63e35ca66d3a969f7d123ac4f67e5dcd7fe`

```dockerfile
```

-	Layers:
	-	`sha256:a25179590d118b79e69af92d0c626fdfe45bf30c8a60c73d2c9e29dcb0f145e0`  
		Last Modified: Thu, 26 Jun 2025 23:57:01 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:d01fc7956bcde73411ae93b65ce5f0416787873edc18c6ab3490b1df02ce8802
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
$ docker pull nats@sha256:3fa9fb2909a6d5fc3d03311c4eab7ef44d9d3b07d3060dc3ee09af31615177bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c303eb1d766fef145d081a6efe6667caecdc3d29274580e7cab2c86b555054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2d7c33042de7a2721cc7037921866dd5fd1aef06251cb3b52b803e099650f`  
		Last Modified: Thu, 26 Jun 2025 20:17:43 GMT  
		Size: 6.8 MB (6788052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23999ece2fd82b549915d209c1220df0e2118a8ba5002f08029344c1b4c11b0`  
		Last Modified: Thu, 26 Jun 2025 20:17:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473fef627e81d8cb609092fc5c8cf8b1c63b551ea1b7efabc4ada599bf6b93f3`  
		Last Modified: Thu, 26 Jun 2025 20:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2d087fb959da797f20ae030821cfc23d2ad4a64a60d6366c00c3f8688177c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415bcb886edb909afed1be06569934e7e858ecf295a54aeae89dc46df442b4e`

```dockerfile
```

-	Layers:
	-	`sha256:26b50ad7dfc22e733e46076788aac20cdb3cb8016ce575e3c885503970de2efe`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c407538f141e101cffc6e93ccea6056debe88221abe2666fcea1e76e978812b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10006784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fa8e3a02d934ff0b1507d42fb94e003f944d9c99c410ca998b4f326cb18384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370714c9df343e678c36a394cbc10501b516beab6c5fce69b58b9bebf4249a9f`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 6.5 MB (6504885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126d04e62112930571ace072c0e66e0b6675f7baa4361daebdcc841a347d84c`  
		Last Modified: Thu, 26 Jun 2025 20:17:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8f8539d59dec90772e674c4b9d02b82a9a630df9678a144bcdf9b36bfa563`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:110e8fc0265af245af68f4f13c82bbd22b526e04b3efed7ac6b206d8544346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7a4b99bc73e5fed3010341026e1d528fbf8f910430925d5aefad24bd4df24`

```dockerfile
```

-	Layers:
	-	`sha256:63caa9adf894da2e6e7743936db5d2d122c600e87b80f1315f63e09ce065c928`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:6beb24b9c5ebaf82aa943605e27bf9cc476073c8ba8a85cf1280e7f903933f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9713025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136c6734a14713ef2df657e7b0afeebc4cac53bb1534f54ef1aaf65d1496933c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b94f9506f9f064db25cf04c1de8c94a0f38399389559a320a9bd4bc11f36e7`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 6.5 MB (6492872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158ea2e3a8384adabb2841e2c82603996443c7dc1a808409ac833bbb51029bb`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e59c609640e45233cbb6721667b61baf5f41cff04c3aff825f166c256bee8`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:70765a6f52b790a1246aa15f97c5d982ac1713fa15c251166982d64ec0a5105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52f6b5f6952440758f161a0c7d3b81e299eb2dc579e6179005f62cec504fd4`

```dockerfile
```

-	Layers:
	-	`sha256:5cd3d0a59672dc8da2c92f06824e2b3654d7aeabd529807d6ecf94d9359b5b74`  
		Last Modified: Thu, 26 Jun 2025 23:56:52 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:12f12a82b812d423ae207b4141ff201258813ec9f30a193037818728c969566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10418482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374b467684dc7a7db213ff191ce7d1f2a1545e87c1ebaa2be4aaff0ba71a099`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75474851f507bad54fde1240afe8e8675cd3e4efc177feaebfd6827dc03b482`  
		Last Modified: Thu, 26 Jun 2025 20:17:20 GMT  
		Size: 6.3 MB (6281567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e96f64006c69ac5cd0996766a85be50bc52bda9d77638f9945484be8249ca7`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c3b4a2c9816edaebe425e51b5e596ed27ce69bbe5dce0089042c23add9303`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5bcd0e65eb6744edfa21188c85939ea1d7cda6f477a5bbaeeaacf9a38f1ff062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0c482c58bc50b5774f0872abe58b788bda3f26499322cbd7f38a109b0f0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f51693de89b45487e48ff77661b758d94f3f9e18c237c375453017a1231744c2`  
		Last Modified: Thu, 26 Jun 2025 23:56:55 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ddd473e4e868ef144ab2d5f9abcf42c5aceb876bb300e0462eebdce5b5f4365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9993129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3072336f828630ea7d0a85fddecbc6eabebebd8559b6776f8c147644cd82c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159dad19c10b3c7682120f345b7e0bea109f9dc391d3a6298d08bb73333d0d59`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 6.3 MB (6261972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7da33fc1b61ecaa43d6f5263a61080be1abe619a070602456f19bceb387f9`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bf6ec9ca48ef6c50947528477f4c16fe8962572e753fa9eedf239e7a401d6`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1e62dcb2bca95114e545acb0e8eff4519f82ce2c57e19687417b288fdbba243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b3c37868ee7b203fddfa4880a0d115e7eb39dec597e967526e3e5fb7a1c4b`

```dockerfile
```

-	Layers:
	-	`sha256:6350f0107c438cca60d4c50ae102aa1fe39670abe71ee66abb23ef856a39ff57`  
		Last Modified: Thu, 26 Jun 2025 23:56:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:676fffad9a719885389d89b25e2658f6b2ffa7ebf49d017b66ae4a959ebd289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6813d2b43b6ca6d4ac54bbb01882cc4ba4237439563dab91499d3ffaf82f9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a12b839b5ac673697b1e2b1c5a3d8e70bc89003735107be2f7098d9a78cea3`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 6.6 MB (6627459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76d719b63c12d9d553830608ff5b6d62b6b8850a3c833d5f108a4e723e1b92`  
		Last Modified: Thu, 26 Jun 2025 20:18:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f6461fda1985f859fa469248cbde00cb5b9a94c750d36727a4fa2fa821f14`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bdcd1a152276665c728f50c64b1ccd43dbdfa0f1532f221e6b409ba7bdb4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f9b5a91c52b3b977a6297761fe63e35ca66d3a969f7d123ac4f67e5dcd7fe`

```dockerfile
```

-	Layers:
	-	`sha256:a25179590d118b79e69af92d0c626fdfe45bf30c8a60c73d2c9e29dcb0f145e0`  
		Last Modified: Thu, 26 Jun 2025 23:57:01 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:a1f720e8485fc0754df5e29fbe72679bcab8bd4234fd92de23ee6bda4a7338e1
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
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:168bb09c4a054a7dec1b1edccdbdc524f9edd8fcec70d4a1cdc9d2201e9c44db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:168bb09c4a054a7dec1b1edccdbdc524f9edd8fcec70d4a1cdc9d2201e9c44db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:a1f720e8485fc0754df5e29fbe72679bcab8bd4234fd92de23ee6bda4a7338e1
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
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:ba84c77cfa19323fd377034bb18a360dc69318846089272b1ea586b7d8101aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:b33dad99cd236d1e37cc4eb8ed9206b6316eda4c64187adc7f1e65ffce3cdb72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287473702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3e602d1e1e318a7bbb885b4a46c7d27f44a285183c5babf5d78687759b53`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 20:17:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.5/nats-server-v2.11.5-windows-amd64.zip
# Thu, 26 Jun 2025 20:17:15 GMT
ENV NATS_SERVER_SHASUM=32b71f33c65cbee21894a2a7b82e5e8f0d7b15071ed591a115637ae9bbf67fc5
# Thu, 26 Jun 2025 20:17:32 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Jun 2025 20:17:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Jun 2025 20:17:53 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 20:17:54 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 20:17:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 20:17:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1c92883cf6e9b17042332de88a3dc30e79476a8df292435d274ff25663a63`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363721f0db417ab1ab377e6bf9123acf262a0b35c2c361e1026c89439c93c089`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5558cc62efdd7b0998e08a4ecfa776ef70871516275984b80a192f2c15ac5b5a`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa5c078273d6cf527c751ed1c752110b3a862d0f746ef91c23feea7ca14353`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b2cfcd8172bc275be5a4eef1b7fb8b868b5c35c2ae018f62cd580e0a9ec74c`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e632d9a39cdd638851c72936a39eebbcf700962d71ce0fce0ab1a6463fcd76`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 352.0 KB (352026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcaa6c58043c1e708d7ebe440178de6af7dd752846fe9dadaf8e69dc67357c`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 6.9 MB (6857935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba4e672ef32c33580896edc49992582d020ca5ee032917311bf0eb466dfde1`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74212ea9e5dfddac2be0bf465d397594828dd1c10415d6c523b647fa3738834`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb92634ba25710d95df0eec641298bc77fbb7eab9879e0681faf82f0e6aa2d8`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecdd379742fa5e86e868683db8922cc7e21ff8a9d87e7e55eec7c3277575a77`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ba84c77cfa19323fd377034bb18a360dc69318846089272b1ea586b7d8101aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:b33dad99cd236d1e37cc4eb8ed9206b6316eda4c64187adc7f1e65ffce3cdb72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287473702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3e602d1e1e318a7bbb885b4a46c7d27f44a285183c5babf5d78687759b53`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 20:17:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.5/nats-server-v2.11.5-windows-amd64.zip
# Thu, 26 Jun 2025 20:17:15 GMT
ENV NATS_SERVER_SHASUM=32b71f33c65cbee21894a2a7b82e5e8f0d7b15071ed591a115637ae9bbf67fc5
# Thu, 26 Jun 2025 20:17:32 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Jun 2025 20:17:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Jun 2025 20:17:53 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 20:17:54 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 20:17:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 20:17:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1c92883cf6e9b17042332de88a3dc30e79476a8df292435d274ff25663a63`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363721f0db417ab1ab377e6bf9123acf262a0b35c2c361e1026c89439c93c089`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5558cc62efdd7b0998e08a4ecfa776ef70871516275984b80a192f2c15ac5b5a`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa5c078273d6cf527c751ed1c752110b3a862d0f746ef91c23feea7ca14353`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b2cfcd8172bc275be5a4eef1b7fb8b868b5c35c2ae018f62cd580e0a9ec74c`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e632d9a39cdd638851c72936a39eebbcf700962d71ce0fce0ab1a6463fcd76`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 352.0 KB (352026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcaa6c58043c1e708d7ebe440178de6af7dd752846fe9dadaf8e69dc67357c`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 6.9 MB (6857935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba4e672ef32c33580896edc49992582d020ca5ee032917311bf0eb466dfde1`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74212ea9e5dfddac2be0bf465d397594828dd1c10415d6c523b647fa3738834`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb92634ba25710d95df0eec641298bc77fbb7eab9879e0681faf82f0e6aa2d8`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecdd379742fa5e86e868683db8922cc7e21ff8a9d87e7e55eec7c3277575a77`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.6`

**does not exist** (yet?)

## `nats:2.11.6-alpine`

**does not exist** (yet?)

## `nats:2.11.6-alpine3.22`

**does not exist** (yet?)

## `nats:2.11.6-linux`

**does not exist** (yet?)

## `nats:2.11.6-nanoserver`

**does not exist** (yet?)

## `nats:2.11.6-nanoserver-ltsc2022`

**does not exist** (yet?)

## `nats:2.11.6-scratch`

**does not exist** (yet?)

## `nats:2.11.6-windowsservercore`

**does not exist** (yet?)

## `nats:2.11.6-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `nats:alpine`

```console
$ docker pull nats@sha256:d01fc7956bcde73411ae93b65ce5f0416787873edc18c6ab3490b1df02ce8802
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
$ docker pull nats@sha256:3fa9fb2909a6d5fc3d03311c4eab7ef44d9d3b07d3060dc3ee09af31615177bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c303eb1d766fef145d081a6efe6667caecdc3d29274580e7cab2c86b555054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2d7c33042de7a2721cc7037921866dd5fd1aef06251cb3b52b803e099650f`  
		Last Modified: Thu, 26 Jun 2025 20:17:43 GMT  
		Size: 6.8 MB (6788052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23999ece2fd82b549915d209c1220df0e2118a8ba5002f08029344c1b4c11b0`  
		Last Modified: Thu, 26 Jun 2025 20:17:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473fef627e81d8cb609092fc5c8cf8b1c63b551ea1b7efabc4ada599bf6b93f3`  
		Last Modified: Thu, 26 Jun 2025 20:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2d087fb959da797f20ae030821cfc23d2ad4a64a60d6366c00c3f8688177c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415bcb886edb909afed1be06569934e7e858ecf295a54aeae89dc46df442b4e`

```dockerfile
```

-	Layers:
	-	`sha256:26b50ad7dfc22e733e46076788aac20cdb3cb8016ce575e3c885503970de2efe`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c407538f141e101cffc6e93ccea6056debe88221abe2666fcea1e76e978812b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10006784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fa8e3a02d934ff0b1507d42fb94e003f944d9c99c410ca998b4f326cb18384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370714c9df343e678c36a394cbc10501b516beab6c5fce69b58b9bebf4249a9f`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 6.5 MB (6504885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126d04e62112930571ace072c0e66e0b6675f7baa4361daebdcc841a347d84c`  
		Last Modified: Thu, 26 Jun 2025 20:17:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8f8539d59dec90772e674c4b9d02b82a9a630df9678a144bcdf9b36bfa563`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:110e8fc0265af245af68f4f13c82bbd22b526e04b3efed7ac6b206d8544346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7a4b99bc73e5fed3010341026e1d528fbf8f910430925d5aefad24bd4df24`

```dockerfile
```

-	Layers:
	-	`sha256:63caa9adf894da2e6e7743936db5d2d122c600e87b80f1315f63e09ce065c928`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:6beb24b9c5ebaf82aa943605e27bf9cc476073c8ba8a85cf1280e7f903933f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9713025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136c6734a14713ef2df657e7b0afeebc4cac53bb1534f54ef1aaf65d1496933c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b94f9506f9f064db25cf04c1de8c94a0f38399389559a320a9bd4bc11f36e7`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 6.5 MB (6492872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158ea2e3a8384adabb2841e2c82603996443c7dc1a808409ac833bbb51029bb`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e59c609640e45233cbb6721667b61baf5f41cff04c3aff825f166c256bee8`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:70765a6f52b790a1246aa15f97c5d982ac1713fa15c251166982d64ec0a5105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52f6b5f6952440758f161a0c7d3b81e299eb2dc579e6179005f62cec504fd4`

```dockerfile
```

-	Layers:
	-	`sha256:5cd3d0a59672dc8da2c92f06824e2b3654d7aeabd529807d6ecf94d9359b5b74`  
		Last Modified: Thu, 26 Jun 2025 23:56:52 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:12f12a82b812d423ae207b4141ff201258813ec9f30a193037818728c969566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10418482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374b467684dc7a7db213ff191ce7d1f2a1545e87c1ebaa2be4aaff0ba71a099`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75474851f507bad54fde1240afe8e8675cd3e4efc177feaebfd6827dc03b482`  
		Last Modified: Thu, 26 Jun 2025 20:17:20 GMT  
		Size: 6.3 MB (6281567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e96f64006c69ac5cd0996766a85be50bc52bda9d77638f9945484be8249ca7`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c3b4a2c9816edaebe425e51b5e596ed27ce69bbe5dce0089042c23add9303`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5bcd0e65eb6744edfa21188c85939ea1d7cda6f477a5bbaeeaacf9a38f1ff062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0c482c58bc50b5774f0872abe58b788bda3f26499322cbd7f38a109b0f0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f51693de89b45487e48ff77661b758d94f3f9e18c237c375453017a1231744c2`  
		Last Modified: Thu, 26 Jun 2025 23:56:55 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:ddd473e4e868ef144ab2d5f9abcf42c5aceb876bb300e0462eebdce5b5f4365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9993129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3072336f828630ea7d0a85fddecbc6eabebebd8559b6776f8c147644cd82c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159dad19c10b3c7682120f345b7e0bea109f9dc391d3a6298d08bb73333d0d59`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 6.3 MB (6261972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7da33fc1b61ecaa43d6f5263a61080be1abe619a070602456f19bceb387f9`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bf6ec9ca48ef6c50947528477f4c16fe8962572e753fa9eedf239e7a401d6`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1e62dcb2bca95114e545acb0e8eff4519f82ce2c57e19687417b288fdbba243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b3c37868ee7b203fddfa4880a0d115e7eb39dec597e967526e3e5fb7a1c4b`

```dockerfile
```

-	Layers:
	-	`sha256:6350f0107c438cca60d4c50ae102aa1fe39670abe71ee66abb23ef856a39ff57`  
		Last Modified: Thu, 26 Jun 2025 23:56:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:676fffad9a719885389d89b25e2658f6b2ffa7ebf49d017b66ae4a959ebd289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6813d2b43b6ca6d4ac54bbb01882cc4ba4237439563dab91499d3ffaf82f9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a12b839b5ac673697b1e2b1c5a3d8e70bc89003735107be2f7098d9a78cea3`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 6.6 MB (6627459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76d719b63c12d9d553830608ff5b6d62b6b8850a3c833d5f108a4e723e1b92`  
		Last Modified: Thu, 26 Jun 2025 20:18:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f6461fda1985f859fa469248cbde00cb5b9a94c750d36727a4fa2fa821f14`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bdcd1a152276665c728f50c64b1ccd43dbdfa0f1532f221e6b409ba7bdb4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f9b5a91c52b3b977a6297761fe63e35ca66d3a969f7d123ac4f67e5dcd7fe`

```dockerfile
```

-	Layers:
	-	`sha256:a25179590d118b79e69af92d0c626fdfe45bf30c8a60c73d2c9e29dcb0f145e0`  
		Last Modified: Thu, 26 Jun 2025 23:57:01 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:d01fc7956bcde73411ae93b65ce5f0416787873edc18c6ab3490b1df02ce8802
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
$ docker pull nats@sha256:3fa9fb2909a6d5fc3d03311c4eab7ef44d9d3b07d3060dc3ee09af31615177bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c303eb1d766fef145d081a6efe6667caecdc3d29274580e7cab2c86b555054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f2d7c33042de7a2721cc7037921866dd5fd1aef06251cb3b52b803e099650f`  
		Last Modified: Thu, 26 Jun 2025 20:17:43 GMT  
		Size: 6.8 MB (6788052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23999ece2fd82b549915d209c1220df0e2118a8ba5002f08029344c1b4c11b0`  
		Last Modified: Thu, 26 Jun 2025 20:17:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473fef627e81d8cb609092fc5c8cf8b1c63b551ea1b7efabc4ada599bf6b93f3`  
		Last Modified: Thu, 26 Jun 2025 20:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2d087fb959da797f20ae030821cfc23d2ad4a64a60d6366c00c3f8688177c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b415bcb886edb909afed1be06569934e7e858ecf295a54aeae89dc46df442b4e`

```dockerfile
```

-	Layers:
	-	`sha256:26b50ad7dfc22e733e46076788aac20cdb3cb8016ce575e3c885503970de2efe`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c407538f141e101cffc6e93ccea6056debe88221abe2666fcea1e76e978812b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10006784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fa8e3a02d934ff0b1507d42fb94e003f944d9c99c410ca998b4f326cb18384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370714c9df343e678c36a394cbc10501b516beab6c5fce69b58b9bebf4249a9f`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 6.5 MB (6504885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126d04e62112930571ace072c0e66e0b6675f7baa4361daebdcc841a347d84c`  
		Last Modified: Thu, 26 Jun 2025 20:17:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8f8539d59dec90772e674c4b9d02b82a9a630df9678a144bcdf9b36bfa563`  
		Last Modified: Thu, 26 Jun 2025 20:17:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:110e8fc0265af245af68f4f13c82bbd22b526e04b3efed7ac6b206d8544346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7a4b99bc73e5fed3010341026e1d528fbf8f910430925d5aefad24bd4df24`

```dockerfile
```

-	Layers:
	-	`sha256:63caa9adf894da2e6e7743936db5d2d122c600e87b80f1315f63e09ce065c928`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:6beb24b9c5ebaf82aa943605e27bf9cc476073c8ba8a85cf1280e7f903933f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9713025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136c6734a14713ef2df657e7b0afeebc4cac53bb1534f54ef1aaf65d1496933c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b94f9506f9f064db25cf04c1de8c94a0f38399389559a320a9bd4bc11f36e7`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 6.5 MB (6492872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158ea2e3a8384adabb2841e2c82603996443c7dc1a808409ac833bbb51029bb`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e59c609640e45233cbb6721667b61baf5f41cff04c3aff825f166c256bee8`  
		Last Modified: Thu, 26 Jun 2025 20:19:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:70765a6f52b790a1246aa15f97c5d982ac1713fa15c251166982d64ec0a5105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf52f6b5f6952440758f161a0c7d3b81e299eb2dc579e6179005f62cec504fd4`

```dockerfile
```

-	Layers:
	-	`sha256:5cd3d0a59672dc8da2c92f06824e2b3654d7aeabd529807d6ecf94d9359b5b74`  
		Last Modified: Thu, 26 Jun 2025 23:56:52 GMT  
		Size: 14.4 KB (14423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:12f12a82b812d423ae207b4141ff201258813ec9f30a193037818728c969566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10418482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374b467684dc7a7db213ff191ce7d1f2a1545e87c1ebaa2be4aaff0ba71a099`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75474851f507bad54fde1240afe8e8675cd3e4efc177feaebfd6827dc03b482`  
		Last Modified: Thu, 26 Jun 2025 20:17:20 GMT  
		Size: 6.3 MB (6281567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e96f64006c69ac5cd0996766a85be50bc52bda9d77638f9945484be8249ca7`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c3b4a2c9816edaebe425e51b5e596ed27ce69bbe5dce0089042c23add9303`  
		Last Modified: Thu, 26 Jun 2025 20:17:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5bcd0e65eb6744edfa21188c85939ea1d7cda6f477a5bbaeeaacf9a38f1ff062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0c482c58bc50b5774f0872abe58b788bda3f26499322cbd7f38a109b0f0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f51693de89b45487e48ff77661b758d94f3f9e18c237c375453017a1231744c2`  
		Last Modified: Thu, 26 Jun 2025 23:56:55 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ddd473e4e868ef144ab2d5f9abcf42c5aceb876bb300e0462eebdce5b5f4365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9993129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3072336f828630ea7d0a85fddecbc6eabebebd8559b6776f8c147644cd82c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159dad19c10b3c7682120f345b7e0bea109f9dc391d3a6298d08bb73333d0d59`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 6.3 MB (6261972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7da33fc1b61ecaa43d6f5263a61080be1abe619a070602456f19bceb387f9`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bf6ec9ca48ef6c50947528477f4c16fe8962572e753fa9eedf239e7a401d6`  
		Last Modified: Thu, 26 Jun 2025 20:19:09 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1e62dcb2bca95114e545acb0e8eff4519f82ce2c57e19687417b288fdbba243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461b3c37868ee7b203fddfa4880a0d115e7eb39dec597e967526e3e5fb7a1c4b`

```dockerfile
```

-	Layers:
	-	`sha256:6350f0107c438cca60d4c50ae102aa1fe39670abe71ee66abb23ef856a39ff57`  
		Last Modified: Thu, 26 Jun 2025 23:56:58 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:676fffad9a719885389d89b25e2658f6b2ffa7ebf49d017b66ae4a959ebd289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6813d2b43b6ca6d4ac54bbb01882cc4ba4237439563dab91499d3ffaf82f9e5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 18:55:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='340fc1ef4162df1c597ef2a13b375b2efe6769d44371b3f2a89969027ece9d8b' ;; 		armhf) natsArch='arm6'; sha256='5beba27af67281eaf42b9c1fc7e91eba276569fad5884342711c44ee9cb10409' ;; 		armv7) natsArch='arm7'; sha256='011498aba59007407523776b14f6f3777dd9afbec7092f8d60c92ce09dc552cc' ;; 		x86_64) natsArch='amd64'; sha256='b89a758f6d9fe294b9bb3d10982efbf5709f4a21fd6b0a702c2e8e1e265affec' ;; 		x86) natsArch='386'; sha256='e5bbb34f6b2b71339daafb6711e2ee81f1ee63593df9f4bd0bcbd29d6e023b2e' ;; 		s390x) natsArch='s390x'; sha256='6e257d30747950d4886f4c88cdefeaf91f3cf4425257cf63f421f32ebaff5e1d' ;; 		ppc64le) natsArch='ppc64le'; sha256='be9d1012adbeb51b7c7e155ef2199e8fe7db50b09569a1a97acaa76ce6f88786' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a12b839b5ac673697b1e2b1c5a3d8e70bc89003735107be2f7098d9a78cea3`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 6.6 MB (6627459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76d719b63c12d9d553830608ff5b6d62b6b8850a3c833d5f108a4e723e1b92`  
		Last Modified: Thu, 26 Jun 2025 20:18:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f6461fda1985f859fa469248cbde00cb5b9a94c750d36727a4fa2fa821f14`  
		Last Modified: Thu, 26 Jun 2025 20:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bdcd1a152276665c728f50c64b1ccd43dbdfa0f1532f221e6b409ba7bdb4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f9b5a91c52b3b977a6297761fe63e35ca66d3a969f7d123ac4f67e5dcd7fe`

```dockerfile
```

-	Layers:
	-	`sha256:a25179590d118b79e69af92d0c626fdfe45bf30c8a60c73d2c9e29dcb0f145e0`  
		Last Modified: Thu, 26 Jun 2025 23:57:01 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:47710a58674c152355730c69fc89d5a86369e3d6d1329cc91767650ce8e0dde6
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
	-	windows version 10.0.20348.3807; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:a1f720e8485fc0754df5e29fbe72679bcab8bd4234fd92de23ee6bda4a7338e1
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
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:168bb09c4a054a7dec1b1edccdbdc524f9edd8fcec70d4a1cdc9d2201e9c44db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:168bb09c4a054a7dec1b1edccdbdc524f9edd8fcec70d4a1cdc9d2201e9c44db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:20a2cf191c919e8d29b97f731a6fece916f205645f3e4b4983ccca9840f4ac31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129048626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c873ecec6ddd432242be8851bf7726a299bf356025fb5f2ed1df5ce1a03292`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Thu, 26 Jun 2025 21:08:14 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 21:08:17 GMT
RUN cmd /S /C #(nop) COPY file:2707c1337304e3183f48883ca75ece5d2201821ff794284a699294a95a5224a8 in C:\nats-server.exe 
# Thu, 26 Jun 2025 21:08:18 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 21:08:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 21:08:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 21:08:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f62bb6aae7856682a51b9e120221d8ab6b98827503996bbd5b48adb687872fc`  
		Last Modified: Thu, 26 Jun 2025 21:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c628963a74f0c67184782213380c0dfbd7161922bd84926d1a4bca3b5d2ed2`  
		Last Modified: Thu, 26 Jun 2025 21:10:12 GMT  
		Size: 6.5 MB (6502296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddcde16be5b3eee8abcd20b7bc309bcc27aa0e06f5a9e4f850fbf5ab9485dae`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040107a4295d8af94518e83a800ecd9e68cf7daf7646ce696569382d07dbfba3`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77ea1911732510e89f01a53feac29d4502403f3df106ccd1ef99dffd1dccda`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45162ad8785004fecd1fde8b2626b8db3a42906765dcd0b0225b8ccd2833c327`  
		Last Modified: Thu, 26 Jun 2025 21:10:11 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:a1f720e8485fc0754df5e29fbe72679bcab8bd4234fd92de23ee6bda4a7338e1
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
$ docker pull nats@sha256:1b8b9649d49fa2e30069448b7a229ffa2875b861cf4dd1b23411961a0cdae9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d44db644f5180de87cc768a529932a9420b6d4ccfbc852e6a795db73b6b5fc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b986fdf486ba4635852d01f4c2b7bd44dc1365e6a39b831dfaafb54cc1c1749c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.3 MB (6329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b079c94293516c2afeadfc553ba92e0e852739ebdffde9a5122852ba1738aab5`  
		Last Modified: Thu, 26 Jun 2025 21:52:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:81a9f6ae969d7c0f2ecdd91aa35de2d82b8599fd5b54300d33370629aa5a17f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4609e9a18a94e027a6b3d4c1b1b539e99faadf0101ec798f3baa952149e0fa`

```dockerfile
```

-	Layers:
	-	`sha256:a16a58ddbdec1a9796a7d5222cd811632fcd48c5069806f81a56aa0624e57b26`  
		Last Modified: Thu, 26 Jun 2025 23:56:31 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b92b71bdb49eeedf86d383fd7d6cc2b0605e51927c33a6a9d8db7d9e5819350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a26f663b545cd77e45a08ccd8b83930c4863549fe66e2be988ed43602c216a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95edf320291a75147132bff81ae41c6070d592bcbe508b42fbf916e4f502d31c`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6042055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d67cd8556ae2d5d8e7a19d754414d6e586e5db39d91a80be92f4e53bfd96`  
		Last Modified: Thu, 26 Jun 2025 21:07:25 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4f430d9a0be9975502386f95a5e0c2b302a4fb893957100eb210b089c6c875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f89405e28c0e3e3f183cd44cf975a2c8a2423850c44f8e97b2e7d8ee9dd91e0`

```dockerfile
```

-	Layers:
	-	`sha256:79fa120485238f3f7210fce9dc1705e897e340b46583dc7c0d6ef19b551ea82a`  
		Last Modified: Thu, 26 Jun 2025 23:56:35 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:dd26c223d82077f133bec95946e7a71766129a0e7ca5fcdefbc7203c8320ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9371d21cc96985dba9edab8bd2d10b25aed4f46afea29adbf9f35574a8d502c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7e9ab7bbd68adaac79b2a92ea44b5fa72116d15f7a0f4989754bd6152f2df201`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 6.0 MB (6033048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ab102dc90086b949d10313d06ea56ac15541fb420954b55eb461509023ee9`  
		Last Modified: Thu, 26 Jun 2025 21:07:36 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6bb3b6db4e0d9548d3e32e7356a552083d7b387b7afb5ed3b6d0e98e5145b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426732dca807620df9889d34e611a6d464dff00125d96233f3a852ecfe55636`

```dockerfile
```

-	Layers:
	-	`sha256:54b76c3c78d78705cba98a2dc65e04782eee61754fc72f2a0d88c4ee47c86e91`  
		Last Modified: Thu, 26 Jun 2025 23:56:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1ec4bf8cd5103eb5a381bd0005848af403d8d5e92e0bb59e816b31946e79892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611a296760a2216a871c1ba63acdde672fffb0f1d833e24fed7f7b0609f289ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9a6e187d23ad87ff0ca1565f86287fa14ddca36d82b4ca19c639768b801a799e`  
		Last Modified: Thu, 26 Jun 2025 18:56:57 GMT  
		Size: 5.8 MB (5795474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a86d8beb005e366c84d6793e932e1364175fa60e98a9bc3ac9d01e8571800`  
		Last Modified: Thu, 26 Jun 2025 21:08:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:543f0814811281806cc9fadceea565c2b1b48cadb5685510eb3ddf8b7dc8d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485941ea2cd18ab6fd28886c4474716695f0cc12c35fa5048bd4957a2d928ed7`

```dockerfile
```

-	Layers:
	-	`sha256:2b195eceabd0143453b428a86464dbede79d86a4e61f67cf4773c1b3c2ce65e7`  
		Last Modified: Thu, 26 Jun 2025 23:56:45 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:ba84c77cfa19323fd377034bb18a360dc69318846089272b1ea586b7d8101aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:windowsservercore` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:b33dad99cd236d1e37cc4eb8ed9206b6316eda4c64187adc7f1e65ffce3cdb72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287473702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3e602d1e1e318a7bbb885b4a46c7d27f44a285183c5babf5d78687759b53`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 20:17:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.5/nats-server-v2.11.5-windows-amd64.zip
# Thu, 26 Jun 2025 20:17:15 GMT
ENV NATS_SERVER_SHASUM=32b71f33c65cbee21894a2a7b82e5e8f0d7b15071ed591a115637ae9bbf67fc5
# Thu, 26 Jun 2025 20:17:32 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Jun 2025 20:17:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Jun 2025 20:17:53 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 20:17:54 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 20:17:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 20:17:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1c92883cf6e9b17042332de88a3dc30e79476a8df292435d274ff25663a63`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363721f0db417ab1ab377e6bf9123acf262a0b35c2c361e1026c89439c93c089`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5558cc62efdd7b0998e08a4ecfa776ef70871516275984b80a192f2c15ac5b5a`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa5c078273d6cf527c751ed1c752110b3a862d0f746ef91c23feea7ca14353`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b2cfcd8172bc275be5a4eef1b7fb8b868b5c35c2ae018f62cd580e0a9ec74c`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e632d9a39cdd638851c72936a39eebbcf700962d71ce0fce0ab1a6463fcd76`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 352.0 KB (352026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcaa6c58043c1e708d7ebe440178de6af7dd752846fe9dadaf8e69dc67357c`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 6.9 MB (6857935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba4e672ef32c33580896edc49992582d020ca5ee032917311bf0eb466dfde1`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74212ea9e5dfddac2be0bf465d397594828dd1c10415d6c523b647fa3738834`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb92634ba25710d95df0eec641298bc77fbb7eab9879e0681faf82f0e6aa2d8`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecdd379742fa5e86e868683db8922cc7e21ff8a9d87e7e55eec7c3277575a77`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ba84c77cfa19323fd377034bb18a360dc69318846089272b1ea586b7d8101aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:b33dad99cd236d1e37cc4eb8ed9206b6316eda4c64187adc7f1e65ffce3cdb72
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2287473702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3e602d1e1e318a7bbb885b4a46c7d27f44a285183c5babf5d78687759b53`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Thu, 26 Jun 2025 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_DOCKERIZED=1
# Thu, 26 Jun 2025 20:17:13 GMT
ENV NATS_SERVER=2.11.5
# Thu, 26 Jun 2025 20:17:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.5/nats-server-v2.11.5-windows-amd64.zip
# Thu, 26 Jun 2025 20:17:15 GMT
ENV NATS_SERVER_SHASUM=32b71f33c65cbee21894a2a7b82e5e8f0d7b15071ed591a115637ae9bbf67fc5
# Thu, 26 Jun 2025 20:17:32 GMT
RUN Set-PSDebug -Trace 2
# Thu, 26 Jun 2025 20:17:52 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 26 Jun 2025 20:17:53 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 26 Jun 2025 20:17:54 GMT
EXPOSE 4222 6222 8222
# Thu, 26 Jun 2025 20:17:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 26 Jun 2025 20:17:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a1c92883cf6e9b17042332de88a3dc30e79476a8df292435d274ff25663a63`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363721f0db417ab1ab377e6bf9123acf262a0b35c2c361e1026c89439c93c089`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5558cc62efdd7b0998e08a4ecfa776ef70871516275984b80a192f2c15ac5b5a`  
		Last Modified: Thu, 26 Jun 2025 20:18:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa5c078273d6cf527c751ed1c752110b3a862d0f746ef91c23feea7ca14353`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b2cfcd8172bc275be5a4eef1b7fb8b868b5c35c2ae018f62cd580e0a9ec74c`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e632d9a39cdd638851c72936a39eebbcf700962d71ce0fce0ab1a6463fcd76`  
		Last Modified: Thu, 26 Jun 2025 20:18:18 GMT  
		Size: 352.0 KB (352026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcaa6c58043c1e708d7ebe440178de6af7dd752846fe9dadaf8e69dc67357c`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 6.9 MB (6857935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba4e672ef32c33580896edc49992582d020ca5ee032917311bf0eb466dfde1`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74212ea9e5dfddac2be0bf465d397594828dd1c10415d6c523b647fa3738834`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb92634ba25710d95df0eec641298bc77fbb7eab9879e0681faf82f0e6aa2d8`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecdd379742fa5e86e868683db8922cc7e21ff8a9d87e7e55eec7c3277575a77`  
		Last Modified: Thu, 26 Jun 2025 20:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
