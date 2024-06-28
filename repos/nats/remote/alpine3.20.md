## `nats:alpine3.20`

```console
$ docker pull nats@sha256:b7752304692bc0612b7fbae6add53cdd14059ec83cad1795d78edade6025ef07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:e2e30db3fc65c7da5465eb3914fec69305e7563f03e3867df5338d119e21e5d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9779039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f62ffb6ee9da597aecc0d69894c5d092a087345e1724ab9de02284c28a0d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:21:10 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:21:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:21:13 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:21:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1e4df5a1f3cf89eb0f77e3b34c5c5de1c3f8f85fdd80615f7a7ac719c4c64`  
		Last Modified: Fri, 28 Jun 2024 00:21:48 GMT  
		Size: 6.2 MB (6154221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e90989e1e58c342beebcfdd7e52a6e135ed86cbb8e6d2beae202738e86dacc`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c404c157ca8e663aebc369434d01a47c02769cc4130d39c6d78c39d53611b97c`  
		Last Modified: Fri, 28 Jun 2024 00:21:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:56a0f3e698bd6cca875d84bfa5045899c63ea1d62cf0c8fd4ff61825c8254515
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc38f28001e4437c3d91c79e9b2197628077869f1cba8be078553fedde93209b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:49:22 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:49:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:49:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230fb38a6edbbf77083de85559f5152ae3b311777c9dd9b9a77cd345e2ef1a9`  
		Last Modified: Fri, 28 Jun 2024 00:49:55 GMT  
		Size: 5.8 MB (5829228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d44ee0675e909ab57563695a6a2b878966904a75a85263f0e72dd1ed0c160c8`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90495b6cc7f87482741b7082f3741b256eb21e6cfdc27d7942be704c35c87fbd`  
		Last Modified: Fri, 28 Jun 2024 00:49:54 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:03c790f7614d5305147cfbe13a802116961c23dc974073e5c1c47a0958a2f2fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8917684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47845ca49a26c51a32431b2430c927f60530a103a0675349923926b7e638365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 27 Jun 2024 23:57:34 GMT
ENV NATS_SERVER=2.10.17
# Thu, 27 Jun 2024 23:57:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 27 Jun 2024 23:57:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 27 Jun 2024 23:57:37 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 23:57:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271b97ad66daef2a27f764db5e9c6526a9ace6245fe75809a7fd36907af85c96`  
		Last Modified: Thu, 27 Jun 2024 23:59:11 GMT  
		Size: 5.8 MB (5821851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb9820f63058faf8433d69f24377a8ddbc7bfcaa39a9c88179f5ce77a805b1e`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c6f2c6543de6de291ecda8fc478e72bf9cd75c3897538f79b8ad3c96b3959`  
		Last Modified: Thu, 27 Jun 2024 23:59:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7a8e195d65d3cc41761f20d6096ea5ba6807d005f662b728f4ccf211d7fd018d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c575cad380d3a69b1cd4455c7379e470e33bcce3d1d452af217dfb3d1d2be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:40:49 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:40:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:40:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:40:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:40:52 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:40:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bcaadb25556d78c413948bf3f15b1fe60418c8549bcb7d735d125765553b`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 5.7 MB (5716255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a5a660d7ed2eee907368ea2b49ea669c8ef4d15da9862dc01a2746fe00f93`  
		Last Modified: Fri, 28 Jun 2024 00:41:19 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16824bb28e2cd1047fd6a73ee7c269a18313eb88420ef1eca4f5328c1b91d4d`  
		Last Modified: Fri, 28 Jun 2024 00:41:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:ef70667d93c0ecad4524d625b054176d8c16c680c5bb22c86d570ebb03e855f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9269475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02380e79f865c822dd2cad3842a68fdea53aaae84dbabee35225c862c9ca1304`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:16:44 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:16:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:16:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:16:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:16:50 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:16:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98f0b27ab1846682176f8c385fda83a868dd88cfafe81ef5c61f6d2069b827f`  
		Last Modified: Fri, 28 Jun 2024 00:17:23 GMT  
		Size: 5.7 MB (5696800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d407236b835911ba0dc017c655dafda719134c57ccf323dfdbaaf755f40be0`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e3075158b3d90272a928f2d5739230c51fcd53e2be7ed27895797c80932b8`  
		Last Modified: Fri, 28 Jun 2024 00:17:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:7a0053d6951e4605fa90abbfd9bc1023242f09a1030c4cc9231f82b2c35fdf33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9483906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677a0b0425470241fcd5496a02579335d4b3a917fd90e4a3039788cab194a0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 28 Jun 2024 00:42:55 GMT
ENV NATS_SERVER=2.10.17
# Fri, 28 Jun 2024 00:42:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='0f4f178ff37716396f0451aee98a9c9f7166d5b79c4bb12580a16e32e2e0f128' ;; 		armhf) natsArch='arm6'; sha256='2a47d80a090582ece7933a44600493e66d163322224f79eee64a824685c4eb53' ;; 		armv7) natsArch='arm7'; sha256='56579ff08e6b2bf69f1d4115715653f08faf78ad58f4ed42c3eaec69976e93d2' ;; 		x86_64) natsArch='amd64'; sha256='e712569650b2adddfd57c8c1606e6d927e68601f3cc86bb95224b3446aebc2f6' ;; 		x86) natsArch='386'; sha256='4714a3b4e948a91a7e974eea9c995e15166ba5c3ba6ec80757044b8f9fba4bff' ;; 		s390x) natsArch='s390x'; sha256='1dd52cec5bc405fae3e65661431e89de049342b157244567cd3e36bae23799f3' ;; 		ppc64le) natsArch='ppc64le'; sha256='c8bc98611c8b1e5e34e852740653208b3afc1975a8e1c1ba4b7fb8e202255cc1' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Jun 2024 00:42:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Jun 2024 00:42:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 00:42:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc90be28c1c57fe10e7ee1d696445ec185d2c1c6377244452c899a053aaf7`  
		Last Modified: Fri, 28 Jun 2024 00:43:40 GMT  
		Size: 6.0 MB (6021076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a74aa595b034e477e40a3ed1865ae7d44d2a4e687bc814e66fc27f78bc3964`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0e518eae95c93170f869a26317b2c41dff11ccfa468809d700b35f5cbbeb1`  
		Last Modified: Fri, 28 Jun 2024 00:43:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
