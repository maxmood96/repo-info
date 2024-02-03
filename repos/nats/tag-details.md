<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.19`](#nats2-alpine319)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.19`](#nats210-alpine319)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.10`](#nats21010)
-	[`nats:2.10.10-alpine`](#nats21010-alpine)
-	[`nats:2.10.10-alpine3.19`](#nats21010-alpine319)
-	[`nats:2.10.10-linux`](#nats21010-linux)
-	[`nats:2.10.10-nanoserver`](#nats21010-nanoserver)
-	[`nats:2.10.10-nanoserver-1809`](#nats21010-nanoserver-1809)
-	[`nats:2.10.10-scratch`](#nats21010-scratch)
-	[`nats:2.10.10-windowsservercore`](#nats21010-windowsservercore)
-	[`nats:2.10.10-windowsservercore-1809`](#nats21010-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.24`](#nats2924)
-	[`nats:2.9.24-alpine`](#nats2924-alpine)
-	[`nats:2.9.24-alpine3.18`](#nats2924-alpine318)
-	[`nats:2.9.24-linux`](#nats2924-linux)
-	[`nats:2.9.24-nanoserver`](#nats2924-nanoserver)
-	[`nats:2.9.24-nanoserver-1809`](#nats2924-nanoserver-1809)
-	[`nats:2.9.24-scratch`](#nats2924-scratch)
-	[`nats:2.9.24-windowsservercore`](#nats2924-windowsservercore)
-	[`nats:2.9.24-windowsservercore-1809`](#nats2924-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.19`](#natsalpine319)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:0c14f22c1d228f0341acbfc93d2b4d8c8c9ecc2a59adc402a120860a3b9ba6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:547c0daaf16b524816376456d772bc665e4950404f1b90234f7c656a2e202bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:15f3887ac1a9fa368be6c8ba73ed9b059a242fc326fc69053314b35da04f3915
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9253015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf0ce78758845e9b2506bd7bfd961ace06fdc3057d98df941be3774fce987eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:36:18 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 10:36:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 10:36:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 10:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:36:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93415b1cd5ad2d3093b7a9370b19168947165824ef7c8a93b740218a9b281944`  
		Last Modified: Sat, 27 Jan 2024 10:39:19 GMT  
		Size: 6.0 MB (6009384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a825199ff1a8892808c6be4681c65539b570e5eff3e6aaf1d9c1e61ef0fc9`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76cdae9c9604eee0cfea93daa1e59038e6e713a09709a526e43d8313ab3fb39`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:547c0daaf16b524816376456d772bc665e4950404f1b90234f7c656a2e202bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:15f3887ac1a9fa368be6c8ba73ed9b059a242fc326fc69053314b35da04f3915
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9253015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf0ce78758845e9b2506bd7bfd961ace06fdc3057d98df941be3774fce987eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:36:18 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 10:36:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 10:36:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 10:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:36:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93415b1cd5ad2d3093b7a9370b19168947165824ef7c8a93b740218a9b281944`  
		Last Modified: Sat, 27 Jan 2024 10:39:19 GMT  
		Size: 6.0 MB (6009384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a825199ff1a8892808c6be4681c65539b570e5eff3e6aaf1d9c1e61ef0fc9`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76cdae9c9604eee0cfea93daa1e59038e6e713a09709a526e43d8313ab3fb39`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:fbaad6757f783e35e2e1c17dbfaa01698a745a0b9da612b5ceb03b1125598a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:fbaad6757f783e35e2e1c17dbfaa01698a745a0b9da612b5ceb03b1125598a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:0c14f22c1d228f0341acbfc93d2b4d8c8c9ecc2a59adc402a120860a3b9ba6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:547c0daaf16b524816376456d772bc665e4950404f1b90234f7c656a2e202bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:15f3887ac1a9fa368be6c8ba73ed9b059a242fc326fc69053314b35da04f3915
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9253015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf0ce78758845e9b2506bd7bfd961ace06fdc3057d98df941be3774fce987eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:36:18 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 10:36:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 10:36:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 10:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:36:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93415b1cd5ad2d3093b7a9370b19168947165824ef7c8a93b740218a9b281944`  
		Last Modified: Sat, 27 Jan 2024 10:39:19 GMT  
		Size: 6.0 MB (6009384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a825199ff1a8892808c6be4681c65539b570e5eff3e6aaf1d9c1e61ef0fc9`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76cdae9c9604eee0cfea93daa1e59038e6e713a09709a526e43d8313ab3fb39`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.19`

```console
$ docker pull nats@sha256:547c0daaf16b524816376456d772bc665e4950404f1b90234f7c656a2e202bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:15f3887ac1a9fa368be6c8ba73ed9b059a242fc326fc69053314b35da04f3915
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9253015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf0ce78758845e9b2506bd7bfd961ace06fdc3057d98df941be3774fce987eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:36:18 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 10:36:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 10:36:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 10:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:36:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93415b1cd5ad2d3093b7a9370b19168947165824ef7c8a93b740218a9b281944`  
		Last Modified: Sat, 27 Jan 2024 10:39:19 GMT  
		Size: 6.0 MB (6009384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a825199ff1a8892808c6be4681c65539b570e5eff3e6aaf1d9c1e61ef0fc9`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76cdae9c9604eee0cfea93daa1e59038e6e713a09709a526e43d8313ab3fb39`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:fbaad6757f783e35e2e1c17dbfaa01698a745a0b9da612b5ceb03b1125598a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:fbaad6757f783e35e2e1c17dbfaa01698a745a0b9da612b5ceb03b1125598a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10`

```console
$ docker pull nats@sha256:cd54df1f5187c7134a48e6e2cc96e5215f1a5652feaffd96423d31d53794d656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.10` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-alpine`

```console
$ docker pull nats@sha256:e63c49e02fcd45cf15275ffa0042979a84b672262ae49431411359f4b21cce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-alpine3.19`

```console
$ docker pull nats@sha256:e63c49e02fcd45cf15275ffa0042979a84b672262ae49431411359f4b21cce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.10-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-linux`

```console
$ docker pull nats@sha256:0278dbdb8b65525954bb0dbbedaca358d28f1220ea55da477944ba53f7234d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-nanoserver`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.10-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-nanoserver-1809`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.10-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-scratch`

```console
$ docker pull nats@sha256:0278dbdb8b65525954bb0dbbedaca358d28f1220ea55da477944ba53f7234d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.10.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-windowsservercore`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.10-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.10.10-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-alpine`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-alpine3.18`

```console
$ docker pull nats@sha256:c61470f7f02219eba30d80d086c70a887344412ddcaa0bac7ede31fd51bf180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:32a5529e36dc72ca3f374f337e1675a43984187220d8c345bace6e5298c8f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9275289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8200b00f670f038e7b9d22cc1a84b354a54ff22058a020385be521b7d76128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:40 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 07:59:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:43 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838fe3e73c4fec3df8c68529e0c2d0db030252e1b0bddd1307004474e42f83`  
		Last Modified: Sat, 27 Jan 2024 08:00:31 GMT  
		Size: 5.9 MB (5871746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e67d6ef43abf2a4f2becd0188b2f8073db7e924a8b979a48d22e14c772ee8b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4b2986a63cb011698c93b70a3488b0a1e7c7b9d93cc1cc49e8a07844bf00b`  
		Last Modified: Sat, 27 Jan 2024 08:00:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:fea6a34d9f842a721ec4ff9fd7db1443edeccbe8e78735799788297b665d37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3269c34939eae2825ba4d892ec5308a129ecf3866f9949422a7bae7c6f0a239`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:23:10 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 09:23:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:13 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e444eae1b8c025531df289f89365623557319857e7a35212cb4c5d3ca8bdc597`  
		Last Modified: Sat, 27 Jan 2024 09:24:01 GMT  
		Size: 5.6 MB (5608585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3aa6a7ee5dd7b26b740259001078d3c619fa52cb9f7b0382814ae0f43a58fb`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cf67ff47e23e8483c446adf122923efacd91b0aa54dbd1a664019c962549dc`  
		Last Modified: Sat, 27 Jan 2024 09:23:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:c96ef3dbc0990c158e3942190b615c84e7453e2ab847587147f06d0f9e16c578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8502810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f80bcf8e39259b669e156d062c69267ff48869ac1d300577543c55d1a9ad173`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:41 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 01:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:44 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:44 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421869803c68366e5d3bf5832e78606d98b05387291b327f3f2ef29860a4fa78`  
		Last Modified: Sat, 27 Jan 2024 01:17:35 GMT  
		Size: 5.6 MB (5600423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2001186d1201569453e012d895f6f848051c44c46d0bbded99c8d4395b76e60a`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba04cc21e26fad2d4a1405fdf818805f3430ef5ccbe127f201fa33264953af`  
		Last Modified: Sat, 27 Jan 2024 01:17:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b79d3106d5912b15da5dc10d2136e207438cf83066b2c42fa4b124392280e6b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149a365b092acbbcaf3cc497163285acf0839a94e704aec6ad74e1093afd432c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:43 GMT
ENV NATS_SERVER=2.9.24
# Sat, 27 Jan 2024 00:43:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c6afa824992389dd0f7fa4073eeaa8b842849c71b0b782da11101b68e4e032fd' ;; 		armhf) natsArch='arm6'; sha256='a5ef539629cde74f974691a78a66a4e30a95a88de06040ad579a606931eade4a' ;; 		armv7) natsArch='arm7'; sha256='514e4a1123f82b775d6b17a12d1a7ce10fa8b5a1b86b9a831c09b13a7e6bc9b0' ;; 		x86_64) natsArch='amd64'; sha256='f4d5dc256d758fa42e7cbf2ddcacc2edfc379bedc0bbdcf5fe6cb67ff3a82d7c' ;; 		x86) natsArch='386'; sha256='b477a8e9a28746fce5bdf5333d16469351de2294402085df81126e699399ec48' ;; 		s390x) natsArch='s390x'; sha256='1b324741684fc7755769c0a212ddd97c2fa9241b5c29886d47d3982078bacf96' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:46 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d2323864c23a8022e1a1666c4babc173499263bafb1a5ab73455744ababaa`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 5.4 MB (5409632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05bfb44b925edd0e8dad9a15f537aaf59527fb8488928d40d62c9a9c1afaf16`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bec85a860322a7f17047c6764c4418552a0bc978f1b836737b42889ddde844`  
		Last Modified: Sat, 27 Jan 2024 00:44:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-linux`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-linux` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-nanoserver`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-nanoserver-1809`

```console
$ docker pull nats@sha256:73e62a60d396fc48da607c6331930fd0805d167c151c01b5bb6d007d6e730e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:04dfc0fb7c253ad7cc06425afaf83755a891623745f7d9b4b3c1d26f09f5084e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109926528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f308760511a2d142f4e7e157bcc4aee60a2fddfc8d95068108d571da790394`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:17:15 GMT
RUN cmd /S /C #(nop) COPY file:bb76bb5eb2960343e0d31314ed4649c426ed59ad3d060057e2c1038e39265b76 in C:\nats-server.exe 
# Thu, 11 Jan 2024 00:17:16 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:17:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:17:18 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d1a38e007259758a3002c7063aa1d123543275c117035c8cac9ccd30e1f1b0`  
		Last Modified: Thu, 11 Jan 2024 00:18:32 GMT  
		Size: 5.3 MB (5328981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6455e2b47c383137ec2bb5bef5aeb229331027b345c2d08f14135f1ee5d6034`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b09a3551da5ce47e8c7fdc4fd9437b2e46d67f0c5033ac499d4ddb0caaa9e0`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4488ed73414629a19600657dcb357e27539522baf886a146543112d12ecf2db`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357d2bc4b192b40d9b8b3df99265f3425faa6618d305ab3b5f4a36511932231`  
		Last Modified: Thu, 11 Jan 2024 00:18:31 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-scratch`

```console
$ docker pull nats@sha256:92f7e9aef076cfefd13b8ceee7d3c2e603be5a9751c4fa686b9e1595422d97a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.24-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ca5325d2a2c84eca8c4f3e3ba96a4fcf6dc91e97e3d3ebd3bae69f7a126c0e62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea934ed1a17a93225092fac66c8b617c594ecec00debda4eb753479eeadedab2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:c3d82eee52a26292cc80755a2b88f8b80cef5c80fd438c99768cd1c33ca95a9d in /nats-server 
# Wed, 08 Nov 2023 19:22:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:22:59 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:22:59 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:22:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44811b84801c95891b1ccde13fe7e76a1ffd8795cd2a066ac0630ee836c23c2e`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 5.2 MB (5247859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927d64e5da79549425963bee122f44117e41eaa442b01673188effd14c9b236`  
		Last Modified: Wed, 08 Nov 2023 19:23:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4d3ccb1b790e4433d69872d7ddb8377aac40d6f000a66fa5b2795a62122a4f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f1a1ecd1b37c66268f966a88d26fa44b35f70909dedab19c60bfd5aca2035e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:401de119a9fad5bd89c70f5a4d5c70f110d490ae5ab9aa60a7f963686ab297ee in /nats-server 
# Wed, 08 Nov 2023 19:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:49:29 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1d2c1b6f013f4386e7235452bc47cebd8001115c3a6504b418ee5b90071492a`  
		Last Modified: Wed, 08 Nov 2023 19:50:14 GMT  
		Size: 5.0 MB (4984334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5fea0f4bcfa87853f77179e249f0a8a09723aeb1c53882e3036fa6250a4ff5`  
		Last Modified: Wed, 08 Nov 2023 19:50:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:c73b24d4fb1ad910ad2f2bdefe0d18bfec11431afb4da9e3cd2be176e4fd49b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe5b4a001ee28a1308edc00242441032b2afb69148c7ba17f692f75e2c1dba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:cd8c3bf2b10d14de1f76a0617be080153909dadcd658bb62cab16d41a650d3de in /nats-server 
# Wed, 08 Nov 2023 19:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:57:47 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:57:47 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:57:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e2a0a8d03803b71ab2e1e3540de965b9430b493bbd15bb2cb1372a7dd564c76d`  
		Last Modified: Wed, 08 Nov 2023 19:58:32 GMT  
		Size: 5.0 MB (4977470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe9df0b73b8b228e9331792251ba43d36af5e4e898411b4f9b725bb8928231`  
		Last Modified: Wed, 08 Nov 2023 19:58:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.24-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:770e514bf6ca4d8b056bd9d16b7df5f56c45c587ce3c815515051b6588e38325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4785043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75bc6347feea13831461567c92c52c13e9085417ef409fb74364cf63105e346`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 08 Nov 2023 19:40:10 GMT
COPY file:209cf40c58f80a36d8d8c8060f48a598dcf03ae451d8d658f267d02f3ce7bddc in /nats-server 
# Wed, 08 Nov 2023 19:40:11 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 08 Nov 2023 19:40:11 GMT
EXPOSE 4222 6222 8222
# Wed, 08 Nov 2023 19:40:11 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 08 Nov 2023 19:40:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b497fc8beff1c9fb319e3b4b62e22135e8e8d81506ede3ca51365887947a8571`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 4.8 MB (4784535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e7980e0793ef96d07cc5a7d9418109519d7d6982ba49570b90d02b2932c`  
		Last Modified: Wed, 08 Nov 2023 19:40:59 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-windowsservercore`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.24-windowsservercore-1809`

```console
$ docker pull nats@sha256:905254cad870fc2919e872296294e54bf7ab513d6400d455504c0ca0eec98fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:2.9.24-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:75d21e7c7902eb91f89a5405f4c0e5b7a3329c3652cd114bb43321f563c300bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075790613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97920b4526f302e30dbb8562fa9dd559fff513b660f872a04105dbf48264c14f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER=2.9.24
# Thu, 11 Jan 2024 00:14:14 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.24/nats-server-v2.9.24-windows-amd64.zip
# Thu, 11 Jan 2024 00:14:15 GMT
ENV NATS_SERVER_SHASUM=4caa027910bfa0a79f2d1c01739e356df37dae15f1336174d459d2fd3a0e10d2
# Thu, 11 Jan 2024 00:15:16 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:16:53 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:16:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 11 Jan 2024 00:16:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 00:16:55 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 11 Jan 2024 00:16:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4036858212ca6f064e29e285b6d9fa03ce15b2a9315733365884fb0e63ef4`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d277b320c347208832277f2419ff434f7d3eb54c141aaef2fd13edbef678d3`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496adc4ee5773352f6bd338210c71dc187b00d620c569f428499f0f210b9be3`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df4c9701f2982452fad8368df4c07858b3a1a092c8c62bcb8cd913758a6f7f8`  
		Last Modified: Thu, 11 Jan 2024 00:18:22 GMT  
		Size: 442.1 KB (442147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f7ad94a16aaa3c2af8e25e185081bff82045acef35ae26a038eb262ddbb02`  
		Last Modified: Thu, 11 Jan 2024 00:18:21 GMT  
		Size: 5.6 MB (5612769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c4995bb7eee3d4871a429d8322314cde4e0ff81e5cb749c764fca7cf92c1d7`  
		Last Modified: Thu, 11 Jan 2024 00:18:20 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24195e2989aa1fdc7ac3c1085f171f29d2418b5359cca044a76edcfafbbea931`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec415c56b7d4247a28d70321f2f0aaee60eb69b2bfdb33070cb41849604beea`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa158ee5a6da454f8f86c48b302e4e3641d718fc212d085e5fe5e5a07856cf4`  
		Last Modified: Thu, 11 Jan 2024 00:18:19 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:547c0daaf16b524816376456d772bc665e4950404f1b90234f7c656a2e202bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:15f3887ac1a9fa368be6c8ba73ed9b059a242fc326fc69053314b35da04f3915
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9253015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf0ce78758845e9b2506bd7bfd961ace06fdc3057d98df941be3774fce987eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:36:18 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 10:36:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 10:36:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 10:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:36:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93415b1cd5ad2d3093b7a9370b19168947165824ef7c8a93b740218a9b281944`  
		Last Modified: Sat, 27 Jan 2024 10:39:19 GMT  
		Size: 6.0 MB (6009384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a825199ff1a8892808c6be4681c65539b570e5eff3e6aaf1d9c1e61ef0fc9`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76cdae9c9604eee0cfea93daa1e59038e6e713a09709a526e43d8313ab3fb39`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.19`

```console
$ docker pull nats@sha256:547c0daaf16b524816376456d772bc665e4950404f1b90234f7c656a2e202bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:8505f2ef754ccfe5a89419850b077f3675353cca8c55e328df3c97de82946f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9564661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b3427e7bfc380643064592125e5f851754edecc335a9c229e6082118f4cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 03 Feb 2024 09:22:16 GMT
ENV NATS_SERVER=2.10.10
# Sat, 03 Feb 2024 09:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 03 Feb 2024 09:22:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 03 Feb 2024 09:22:18 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Feb 2024 09:22:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdbf3ac150e8178b0567d0971bb7c519ed262977937463a9995bd4e3036fe63`  
		Last Modified: Sat, 03 Feb 2024 09:23:25 GMT  
		Size: 6.2 MB (6154935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05158830a84e126279bcbd6513620356232d8610a605754092beb8eb9cde7ec1`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34469c863cbcb81d47a7150e7cfd757af75339fd76260a56dc681b3dcb564cf9`  
		Last Modified: Sat, 03 Feb 2024 09:23:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:25ba40dd4a63bd2bc1d9ed30dff8824b02a9a0e378e4e684ee6dc1ba718548b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9039707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005114d4dd807654d0bceacafcc8c8959f686490ed0ad1a2664e9e40cb370972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 22:53:35 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:53:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 22:53:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 22:53:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 22:53:40 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 22:53:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d721bfc33333afa24177ed965c7a56f9b715795055b03c385c4a0fe72a50389`  
		Last Modified: Fri, 02 Feb 2024 22:54:17 GMT  
		Size: 5.9 MB (5873310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74057532f477c454db64966fad3cb450992a6030e7c670a454b2840a3936fb3`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb5d0a2603ec44d28672800847767ba8cb9767ba88c441692f2aa6bab434958`  
		Last Modified: Fri, 02 Feb 2024 22:54:16 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:5e2cbd5c773e1ff263937e6e94e5d69cc1ef32978492ad6deab3a516240edf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8784240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47893d8405e6f0cd456a9e6553d305f1a89bb2160c5de430832b4c20cabf0ae1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 23:26:31 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 23:26:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 23:26:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 23:26:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 23:26:38 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 23:26:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f18ea7f4bf3011459dd7f48461cbc3d0f90d772d80002443da74ccec297ec70`  
		Last Modified: Fri, 02 Feb 2024 23:27:27 GMT  
		Size: 5.9 MB (5864342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7008388981794b5909386304e06703f927bc64b0d935d3826126571743ddc81a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeabb9df338e30122b55ce5b91a986d7cea242cb7961f7d46919522f8455c06a`  
		Last Modified: Fri, 02 Feb 2024 23:27:25 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:15f3887ac1a9fa368be6c8ba73ed9b059a242fc326fc69053314b35da04f3915
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9253015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf0ce78758845e9b2506bd7bfd961ace06fdc3057d98df941be3774fce987eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:36:18 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 10:36:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 10:36:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 10:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:36:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93415b1cd5ad2d3093b7a9370b19168947165824ef7c8a93b740218a9b281944`  
		Last Modified: Sat, 27 Jan 2024 10:39:19 GMT  
		Size: 6.0 MB (6009384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a825199ff1a8892808c6be4681c65539b570e5eff3e6aaf1d9c1e61ef0fc9`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76cdae9c9604eee0cfea93daa1e59038e6e713a09709a526e43d8313ab3fb39`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:0c14f22c1d228f0341acbfc93d2b4d8c8c9ecc2a59adc402a120860a3b9ba6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:fbaad6757f783e35e2e1c17dbfaa01698a745a0b9da612b5ceb03b1125598a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:1f5551f5ca68b912ffc3a12705783759fc33553cef8d287b9cf549c015e4b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:36e1ffe25cc3108757a0fa914e80af0dae246a31e8c5ef8af78e470e928eda6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110247648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8239e8a72f473ce20494c7e8a7040e29dcbccb25d12f31882a025a08738a89e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:18:20 GMT
RUN cmd /S /C #(nop) COPY file:4da0f8234ade3a140b7c5ab7aad542163d11d3bb3b44e16168afc22293437b5f in C:\nats-server.exe 
# Fri, 02 Feb 2024 22:18:21 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:22 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:23 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79664b25883ae3fcdfeda27b4da3603832e00eb375b623df53438aa8f0ac646f`  
		Last Modified: Fri, 02 Feb 2024 22:19:33 GMT  
		Size: 5.6 MB (5649982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedf573b3a0321e08e5c8e43427e1406b3ed27ccb0f7d5f74d0a8dcf22995a`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f2c12fd97594b9283ca36d43bde81826f04beac68ef314be1829cb693f5175`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cd6383175f6eae5c6439950a97addcec1afbd63dd9176a0d0d1d10a8f5d0dd`  
		Last Modified: Fri, 02 Feb 2024 22:19:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bd3b85452231cf948247504bd83433af01e4e7831ece283e4cdb36a6d98cd`  
		Last Modified: Fri, 02 Feb 2024 22:19:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:fbaad6757f783e35e2e1c17dbfaa01698a745a0b9da612b5ceb03b1125598a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:fa26beda8a3187ccefa47afcfe9ea6d0e2f40a57c8f64d70bd63c792d7973938
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa17fbc9745c6d9a8844e1ab4bb411caac4d947976e573ea86772f7aa77fc94`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:c08da355ccf630687140908574051bdb27ddac7abffc43539f1c353a915995cb in /nats-server 
# Sat, 03 Feb 2024 09:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 03 Feb 2024 09:22:51 GMT
EXPOSE 4222 6222 8222
# Sat, 03 Feb 2024 09:22:51 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 03 Feb 2024 09:22:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:047025d894a82d5535fd2b9375a9afb4ee6cc12a2b1e4867be9190608b7d0e10`  
		Last Modified: Sat, 03 Feb 2024 09:23:46 GMT  
		Size: 5.5 MB (5534482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bb1b76b38e15129b4ab3f2c13a8104a99b4fcef2c0a3e660b6aaae01fa1458`  
		Last Modified: Sat, 03 Feb 2024 09:23:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:bf131e69ab071b6f35b570adbc6e1cecd2bfe84b3266f6f90f65a608a4b93a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd385de8b290b9955080cae793cf6cc6035d37a033c7372f51b0f14ef3fd00d4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:4258d78e61f143bf9ab22c31b60d52274c67232f99da900403fa34fb76729fb5 in /nats-server 
# Fri, 02 Feb 2024 22:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 22:53:48 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:53:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 22:53:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6ca579f793deefb3bceddd7cc6434a1adce9d85d8fc09de9f54d543ea96b97f`  
		Last Modified: Fri, 02 Feb 2024 22:54:39 GMT  
		Size: 5.3 MB (5251258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09cf38736260e7d6e66ea6a9f76ecfbce658e9595b92187e7a5c609e775e4df`  
		Last Modified: Fri, 02 Feb 2024 22:54:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:4d1b9adf07bca0383a20f3a21531b8d21b8b969c16b1f0598ecfba3348507df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf13f9de87831135f176796dd8eabff25a62f3e951e6e65e4522dd6217976a1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:a5369e97852f33a5b160df764848008d4e49500d87a2e74a481b8edb12653e8e in /nats-server 
# Fri, 02 Feb 2024 23:26:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 23:26:54 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 23:26:54 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 23:26:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f6811f2c3b47fd4f9bfbc306106cab5eaa4a76efcbfb405c5444c3cfca0dcbf`  
		Last Modified: Fri, 02 Feb 2024 23:27:48 GMT  
		Size: 5.2 MB (5243254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b28d09f0aa31c4843e0b7e128993c19c836b0ff361c9187632539ff1eb416a`  
		Last Modified: Fri, 02 Feb 2024 23:27:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:72b3850d5a9af2035c35513106c9f06bf73cca3681e78abd1cc95635edcbfa6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64a905fbeb688b0d47c8c50cb919729a44ec3bc9e3a6d4181968b0652e2fa7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:8296ec99f2edacbd26a36bcbea24c2220019685c80d72189ab30a4ead40b0a0d in /nats-server 
# Fri, 02 Feb 2024 21:54:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 02 Feb 2024 21:54:18 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:54:18 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 02 Feb 2024 21:54:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b73c63f9aa24e1c550000ee6aab1b78e9bc25b97748ad58194fbfb6c6cf673c`  
		Last Modified: Fri, 02 Feb 2024 21:55:14 GMT  
		Size: 5.1 MB (5105599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9835428a911094e35ecc76ef5e5906af872d4c0923381656ac1d2e760789e181`  
		Last Modified: Fri, 02 Feb 2024 21:55:13 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:d0b84ed068b7f0fe00d5ab02f7a8bbb8ebaf90bf657c36463c76b41ac0d50ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69542e675992da4639da6f2c125c0d51560fd34f85b4de29815593a7136e3c38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 17:54:04 GMT
COPY file:62b4ff865435762036d97cf7296ae4eb04b8fffbc5feee5da88fd1a6eca3e5c6 in /nats-server 
# Thu, 11 Jan 2024 17:54:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 17:54:05 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:05 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 17:54:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7224d41d2ed8555b103fcef1a66d70913eb475babd8b1dfea87c7fdfe6620f86`  
		Last Modified: Thu, 11 Jan 2024 17:54:45 GMT  
		Size: 5.4 MB (5384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588d0af47d5bdf74a41af3929e6ec39ddfeabb9aa5a13ffe9debfad15e51626`  
		Last Modified: Thu, 11 Jan 2024 17:54:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:263dc1906c5b5a2332d0b6a46ffc6603ffe9285a2c17792b4656f000c0d11b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats@sha256:f117a76806e0323d616ab3f876137fb624b8547621e54f964fd34cb25486c9c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076135685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929ad88f44da625ee4ed8ae7cab19a27a773275a97a49eb6dd7ed8907a90cd74`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Fri, 02 Feb 2024 22:15:06 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 22:15:07 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.10/nats-server-v2.10.10-windows-amd64.zip
# Fri, 02 Feb 2024 22:15:08 GMT
ENV NATS_SERVER_SHASUM=d135040811bbf093dc9eb84df2db3c895d497133278e4db70f6f5b26b421838c
# Fri, 02 Feb 2024 22:16:21 GMT
RUN Set-PSDebug -Trace 2
# Fri, 02 Feb 2024 22:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 02 Feb 2024 22:18:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 02 Feb 2024 22:18:07 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 22:18:07 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 02 Feb 2024 22:18:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e53ca3719e6e9112088f66f71aaef8bbb197e6092f22f1ba72c850be7530914`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413040ec09514434dca5d5aad02ae31a8c640cf903dac2fa7e664b3d38467ff4`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60133191d49be76203feabf2af44a7cbb53ba8b87d63060935a27d55a156e7c5`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e367ec399c652035faf850e6b86983b298764b8235f63243d25543c43a40`  
		Last Modified: Fri, 02 Feb 2024 22:19:16 GMT  
		Size: 454.2 KB (454247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8116acb67fede86d4954fdd4e3f74a2fbe6dbc59a63cebf20f2d2432fa871bf9`  
		Last Modified: Fri, 02 Feb 2024 22:19:15 GMT  
		Size: 5.9 MB (5945679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74635b53e0ec71d3a86fa2893343f620736a1d8c5479a971d6d59c7a89a8ab`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa627392b90e6e082a6e9f016fc01148762aa2e29a87024d2c0bd7e1b196942`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4c34896adf534815a28f43f4ed0521bc607062da66b18cec2f9593be17011`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbf8f98271f2fc5cf9645300a39dc8d565dd717915e89e8d7d9fa01a753cef2`  
		Last Modified: Fri, 02 Feb 2024 22:19:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
