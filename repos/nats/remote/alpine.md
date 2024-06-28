## `nats:alpine`

```console
$ docker pull nats@sha256:8f5c163cf6a1547423e75f78b98ed556cb7b712c96818f8d9b2b9be44aa23496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

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

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:386cf7209c82925aec5ff62177e677fc1eb71254363052737ced029f1746c2d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9151824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d8c8dcdc96140f9a0b73886603ae9c3cec3e2c1f977f1bc88066063a17b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:05:21 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:05:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:05:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:05:24 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:05:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e7654d76dd1e1a16668be22ce88c527252378ad4783702a94067c0c751a4e`  
		Last Modified: Thu, 20 Jun 2024 18:05:59 GMT  
		Size: 6.0 MB (5976942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9d64e502c2d54025f27ee5d2f49308f269df219584c849d052318a4a2445e3`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07643bccdb4d23338d8a9dc32ab0326aab096b46bc18db5fc0e25b939c2219ae`  
		Last Modified: Thu, 20 Jun 2024 18:05:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

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

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:2a9a47867f6910dcad35ee2adb40e1ebd4f7381cfa7ac8e3d46ee709c9509454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9223832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fc6bee67128e107557890b1d00d25acb81accd54bfacfe6cb953e326f76869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 19:07:34 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 19:07:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 19:07:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 19:07:36 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 19:07:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e89542e528e02fabff19cf627dd2db7429cab490cef7cbf89385ddb608353b`  
		Last Modified: Thu, 20 Jun 2024 19:08:10 GMT  
		Size: 5.9 MB (5865654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee9f2793b2fd1868c61303def6d04454f05cde264b69ffde11ca155b1cfb5a`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fad8c80be0821dada9a573bbbacae2c905429b8c358b82716cec53a0b382f`  
		Last Modified: Thu, 20 Jun 2024 19:08:09 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

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

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:bb4fac87f963387e412ce44f8d57b4a2ae4f7b19d29f9292d255df2205e69e63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9419751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675e4ecaaad8d92ab417e59c137cdc38a8d5514eee32aca6d3361b8a5ce1d3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:02:04 GMT
ENV NATS_SERVER=2.10.16
# Thu, 20 Jun 2024 18:02:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 20 Jun 2024 18:02:07 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 20 Jun 2024 18:02:07 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 18:02:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ac3a0307ef594c85a854ac7d44849a5617e498c64b0b6efc4f4e1939cb8d5a`  
		Last Modified: Thu, 20 Jun 2024 18:02:45 GMT  
		Size: 6.2 MB (6166287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930003305ad08afd656818d360cc14b04b64cb475048a07d491cd516f26149f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945aeca9a2cd276d46df25a26a61cd1b07218667a26d0456f4ec98dc0c0df41f`  
		Last Modified: Thu, 20 Jun 2024 18:02:44 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
