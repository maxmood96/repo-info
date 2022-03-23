## `nats:2-alpine`

```console
$ docker pull nats@sha256:2e7e2ff4d763dc7b53f69888568b7c0d9f49c550e386b2f720f2e9f221757404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2d671bb39b0fe8ccc27e28fc3a0ec14bc446c025e89b793dc1d44f4f9bab2eff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7596864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c549f84fbca77e0876da3c9945554246b9e99bee8a0b0c946c48d3d0f339ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:59:03 GMT
ENV NATS_SERVER=2.7.4
# Wed, 23 Mar 2022 17:59:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 23 Mar 2022 17:59:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 23 Mar 2022 17:59:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 23 Mar 2022 17:59:05 GMT
EXPOSE 4222 6222 8222
# Wed, 23 Mar 2022 17:59:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Mar 2022 17:59:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd1ee64e097f94bfa61c8337bbe6f7b5353fd2db6f2bd16312c16d34219087a`  
		Last Modified: Wed, 23 Mar 2022 17:59:49 GMT  
		Size: 4.8 MB (4783175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df9e0e02cff79130859bbbfada1bc831f04a2492827120162b9d434d87a1a8b`  
		Last Modified: Wed, 23 Mar 2022 17:59:48 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec18bf1e26e76b4d0d04ec2511c92aefb2624fde5238bf2f33da8d115ceceae`  
		Last Modified: Wed, 23 Mar 2022 17:59:48 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:45cbdc6f5cdff383a3d0e0bdb86cce063c0f64bf1f3dad2943ecb07533ad782e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7073602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c737a82b4d492a44c44a46457d0d97e0ad4dbb64e26be5ff889cb3d1d3614c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Mar 2022 02:26:45 GMT
ADD file:9c8618405ef54d562132919ffe49c862d014b402e0e4813b87bf01574fa04c0e in / 
# Thu, 17 Mar 2022 02:26:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 06:05:19 GMT
ENV NATS_SERVER=2.7.4
# Thu, 17 Mar 2022 06:05:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Mar 2022 06:05:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Mar 2022 06:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Mar 2022 06:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Mar 2022 06:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 06:05:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:787f016efa9bc7812361be134f731e845b97fba19169cf3615e7048c0412380e`  
		Last Modified: Thu, 17 Mar 2022 02:28:24 GMT  
		Size: 2.6 MB (2624973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f828906630ee01112a07de0bec229ebca6e306c74e6e0146e258c8e368a7ccc4`  
		Last Modified: Thu, 17 Mar 2022 06:07:25 GMT  
		Size: 4.4 MB (4447630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704a64d737e140c15b6c1459e5c9a23b27d8cb0a4df466b7ec4cc933419b99a1`  
		Last Modified: Thu, 17 Mar 2022 06:07:23 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16383a35c1478cde4438d11efb8e0612109e139cc9f924e874843719ecd0ef9e`  
		Last Modified: Thu, 17 Mar 2022 06:07:23 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:691483abed53be5f73c1d2646fc1e1f0dbff756fc27de2d12f98f6ec24604778
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb42d42e36146d026efb773bae5b2bd1ed4c4dba640cb1967fee43a0b8fc2d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Mar 2022 09:26:34 GMT
ADD file:01e87d7f83dfb32fd8a1b7b889b923432c2e0516d79a4196e01ad0ad15e33d68 in / 
# Thu, 17 Mar 2022 09:26:35 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:11:11 GMT
ENV NATS_SERVER=2.7.4
# Thu, 17 Mar 2022 22:11:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Mar 2022 22:11:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Mar 2022 22:11:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Mar 2022 22:11:16 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Mar 2022 22:11:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:11:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:205cbce5da6d59acc17b2db4c1af7903ca3497b99d4bedb94ef66ace17303808`  
		Last Modified: Thu, 17 Mar 2022 09:28:11 GMT  
		Size: 2.4 MB (2427136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52e366b9e42b5c731370e27c72011013f1c42925992c146dc64a5dddcc16e79`  
		Last Modified: Thu, 17 Mar 2022 22:13:21 GMT  
		Size: 4.4 MB (4441384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79717978f32c52aa40d0931918cd433ba479eff7e01299608ec9d8ba2af0a49e`  
		Last Modified: Thu, 17 Mar 2022 22:13:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdbfc4694a4fb180cbe4bba4b390714bb862b0cc93fdc2d50066bc8ca284d3e`  
		Last Modified: Thu, 17 Mar 2022 22:13:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9b47abd311a5fcd9ab08a15d48e678270aa529450cc455b5e286e4713d09eb53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7142183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79bbdd976c991214406ffc80433570b2d33fb8bc6fa86da9d15883ea2b1b75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 11:44:58 GMT
ENV NATS_SERVER=2.7.4
# Thu, 17 Mar 2022 11:45:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='49457be98663ef3e128b53b56ba45fca216fb6b0d5ba6841605bd8b3984ab698' ;; 		armhf) natsArch='arm6'; sha256='415e9dbb8fa5de697a3b524d31e15af168758465c17b547f329d14fe158192a2' ;; 		armv7) natsArch='arm7'; sha256='2723c8e7806c552b5c08d5823cbcf36ca7c7657794fae9e6adb9b6b4f1feaea4' ;; 		x86_64) natsArch='amd64'; sha256='1885db0c2844fbfbd07f93e036089f210e8e4b6e4cf0ec3890b3724576afc727' ;; 		x86) natsArch='386'; sha256='16d5a990c0c8ee9ecd275fe1e23cede06c0ae7ca93229738ced1df6b97b8ad6d' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Mar 2022 11:45:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Mar 2022 11:45:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Mar 2022 11:45:03 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Mar 2022 11:45:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 11:45:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a69ee1f13e80569d9288ff3e02f2721966a14a3b9c5ee036cb597064624e17`  
		Last Modified: Thu, 17 Mar 2022 11:46:02 GMT  
		Size: 4.4 MB (4426404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057dc966e65974df57b58bfe017dd3791c625365f63c08baa071b77e6f520cc6`  
		Last Modified: Thu, 17 Mar 2022 11:46:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1c2c5fd4aed504126ec28f41a19d7eaa3372313a2ccd1f220814112d9680bd`  
		Last Modified: Thu, 17 Mar 2022 11:46:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
