## `nats:alpine`

```console
$ docker pull nats@sha256:d21d20ce210a5b2ad455f59fb1575e46408b8f3412915236fb9e5b42e2409bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:e3dc3554afb54f24b96cc8b9ed45304e3cdf4af3e0d825513842cccc6443f850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9507519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b77f7441d4a0fb6c985252a186dd754c2bbfffb97adef86dfd317af118334`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:24:10 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:24:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:24:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:24:12 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:24:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f36f68f29c67409263076c2054d9e936c2f5e1a55ee937eb688ec1ce4915b8f`  
		Last Modified: Fri, 27 Oct 2023 19:25:16 GMT  
		Size: 6.1 MB (6104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bd88fc72377412d689508327b2bddbd4b2809fc079dfcead61801da1e9883c`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29d0d1b8451bb92780ecfbc6b0f6488f2dbe6544277150975c6cfe9f22e12e3`  
		Last Modified: Fri, 27 Oct 2023 19:25:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3f88f59fb120cd5be7f12dc9d2fb4b443ff7cd301e1bd95254dc57f4d2ce6561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8970070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07efe60769658973f2765083517eda81ef09d5bb126a31af0295381865319ceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:49:22 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4fa6d23f1c5bfabc6eef228ba8baad859591a66d6499d64906f0f27f6d922`  
		Last Modified: Fri, 27 Oct 2023 19:50:04 GMT  
		Size: 5.8 MB (5823776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfe6a1c19a37a61b685e720cd1156f95339fd4f9a4a425de2d8660166d9262e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3442d93fb16090b52375f2f415c787201447a8ade97b668a970f125f54a37e`  
		Last Modified: Fri, 27 Oct 2023 19:50:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f38e6a15d5aee9730165a0a42dcaff9ecb306765613d8bab7eb1cfe51c7a306b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45868af98d7975ae09eecf8c1ad64a141d32fdb6a194bdf9afafffc05284c7c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:57:32 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:57:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:57:35 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:57:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44387fce322d8b03c5a038b2ba2a5e50919536ca64fd3fd32dddedce21340409`  
		Last Modified: Fri, 27 Oct 2023 19:58:22 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43c9b7450ee82499c6b877fa3b396205a7a4401978c9abd93e1b06200e9e5b0`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59161e165420801f1ca6fba02cdfe0a8f3ba106b5443f1973c93063309ba83a`  
		Last Modified: Fri, 27 Oct 2023 19:58:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b122cc94ebf709dd7ac8dbf611b3cbb93d995761f7a0cf90c9f1bfdc721db30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9012372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1202aa9cd9cdcca825729430f679709284ca27900947697c866d1ced15ae5691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 27 Oct 2023 19:39:47 GMT
ENV NATS_SERVER=2.10.4
# Fri, 27 Oct 2023 19:39:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='38e137d26623cd06687ca560b45a359d184f72418faa8da5185d39aa2251b8c1' ;; 		armhf) natsArch='arm6'; sha256='9dab52843eed706b19d77db1b60611b0e205c862a913206cc7af3c640bbc67d0' ;; 		armv7) natsArch='arm7'; sha256='65d1d774d5a41d9df8e37c4578aac0d415363dc2b6eb27ac4adf86921fdea7c9' ;; 		x86_64) natsArch='amd64'; sha256='bb29fb04df977371ecb9fc3e33d1c9203db4f629a19303fe0c42a69d6ffd40d6' ;; 		x86) natsArch='386'; sha256='6809cd6423fc05f1296b24730d2b96d2803ba5cb65dcd5a906fc09cf9175d131' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Oct 2023 19:39:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Oct 2023 19:39:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Oct 2023 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Oct 2023 19:39:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b401e86e5d329ffd1a089932b1a9105a8375d0b413dc151add60434ed63162d1`  
		Last Modified: Fri, 27 Oct 2023 19:40:42 GMT  
		Size: 5.7 MB (5679544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939868b32dc69dc261c1c70fc9f1e9f3954f898d303b8d4a37e7178c8bf6c58b`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0ee4d1df33e3c8250ff7240533a3ea68875726979421fc6d9f705f0acf8d7`  
		Last Modified: Fri, 27 Oct 2023 19:40:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
