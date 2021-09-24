## `nats:2-alpine`

```console
$ docker pull nats@sha256:4113cdc3cc47c19d7d54c61bc13a5bd926ed0e0e8d03666c17045b1416662442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:14cc6a656f138d1e3e707e88c18ef88452b29ccb72af4176b8f5f78d23748030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7655041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5d1cad0ce15a4e94e87f82b966b73e25ba0d4629eb29c09178beb3f5af0b43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 24 Sep 2021 18:20:14 GMT
ENV NATS_SERVER=2.6.1
# Fri, 24 Sep 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4354bdc411f63fa1528479b39b9312de1e1c23531136d88c6b58978dcbf1ec29' ;; 		armhf) natsArch='arm6'; sha256='65473af9ff2f0c75b65609722ad8eb37ee495b382a16697b0168a02abd7bf0f9' ;; 		armv7) natsArch='arm7'; sha256='c95287f62472566bbe30941b57dc4df6547ea5d6219615c3666ae4d5f3acd9d9' ;; 		x86_64) natsArch='amd64'; sha256='9168ba515d68cce426874096d0be2510d9846de66c74c7ab3ecbdc2a27e9c114' ;; 		x86) natsArch='386'; sha256='8f83456101181c7a0a59e83be03c4ec54d6a34737609d97575e2a4f47a08aa24' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Sep 2021 18:20:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Sep 2021 18:20:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 24 Sep 2021 18:20:18 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Sep 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Sep 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb318bc128d118ab570ff784f370b12bba9799d4b8ead06996ddb459d55ba9f4`  
		Last Modified: Fri, 24 Sep 2021 18:21:22 GMT  
		Size: 4.8 MB (4839621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abea9d20040e530947975d310bc6504f29c3518f07ca9320cf04a81b0372d03`  
		Last Modified: Fri, 24 Sep 2021 18:21:21 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787462ffd44dbb2ccc478572962380ecf84219b3f54034a8244cab789596707`  
		Last Modified: Fri, 24 Sep 2021 18:21:21 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a1a401c2dd42ed8081e7ebf328dd7f9dd6ffe9dad928bd908a2dc7a0961660a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7130757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128ff61bfd32f451b68421543236d227440c88041c46314a65b7b3604efcc7ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Sep 2021 17:49:42 GMT
ENV NATS_SERVER=2.6.1
# Fri, 24 Sep 2021 17:49:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4354bdc411f63fa1528479b39b9312de1e1c23531136d88c6b58978dcbf1ec29' ;; 		armhf) natsArch='arm6'; sha256='65473af9ff2f0c75b65609722ad8eb37ee495b382a16697b0168a02abd7bf0f9' ;; 		armv7) natsArch='arm7'; sha256='c95287f62472566bbe30941b57dc4df6547ea5d6219615c3666ae4d5f3acd9d9' ;; 		x86_64) natsArch='amd64'; sha256='9168ba515d68cce426874096d0be2510d9846de66c74c7ab3ecbdc2a27e9c114' ;; 		x86) natsArch='386'; sha256='8f83456101181c7a0a59e83be03c4ec54d6a34737609d97575e2a4f47a08aa24' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Sep 2021 17:49:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Sep 2021 17:49:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 24 Sep 2021 17:49:49 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Sep 2021 17:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Sep 2021 17:49:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb93c29b9a608654f6f3250d956bd76a6258cd040dcce775e03f76f69b935124`  
		Last Modified: Fri, 24 Sep 2021 17:51:54 GMT  
		Size: 4.5 MB (4502338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07b9b15d4e0d0c308fad89b3cdac4e3ec483cfb76b99d9ebaef8467df2b9044`  
		Last Modified: Fri, 24 Sep 2021 17:51:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ebd3f91acd6d1cb72a6ba50ed3b318d260069adbecd9a3b828c6d1ab0f66db`  
		Last Modified: Fri, 24 Sep 2021 17:51:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:972ab950f2b66e74d87d22da4b1839d39668d5edd9101b890132a231497292eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e52058719acb3fa32fb129feb81f0056b2a7736696b0694669b38a2978d60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 21:32:10 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 21:32:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 21:32:17 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 21:32:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f3df2cbc3c87820b00184dca6f1f0fc56066b82a951efe785873912615010`  
		Last Modified: Wed, 22 Sep 2021 21:34:28 GMT  
		Size: 4.5 MB (4494903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac9dabd3dd6b459696ed61905b261fc5d2119025e1a4f11e4f28ac3148b5eb`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3893e6935065d5383621afd73fa5b94df41b088b8a86c1d0bc95fb287a88ed2c`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38888e1c67f76b7edbb92804a050b5de8e4e4f6ae8a980f919d17de7f1fcd4f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7162092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700188dc91cf1626d6b15bb088a273301826130510c19b4dcc9fa42a7f8592ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Fri, 24 Sep 2021 17:40:05 GMT
ENV NATS_SERVER=2.6.1
# Fri, 24 Sep 2021 17:40:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4354bdc411f63fa1528479b39b9312de1e1c23531136d88c6b58978dcbf1ec29' ;; 		armhf) natsArch='arm6'; sha256='65473af9ff2f0c75b65609722ad8eb37ee495b382a16697b0168a02abd7bf0f9' ;; 		armv7) natsArch='arm7'; sha256='c95287f62472566bbe30941b57dc4df6547ea5d6219615c3666ae4d5f3acd9d9' ;; 		x86_64) natsArch='amd64'; sha256='9168ba515d68cce426874096d0be2510d9846de66c74c7ab3ecbdc2a27e9c114' ;; 		x86) natsArch='386'; sha256='8f83456101181c7a0a59e83be03c4ec54d6a34737609d97575e2a4f47a08aa24' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Sep 2021 17:40:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Sep 2021 17:40:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 24 Sep 2021 17:40:08 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Sep 2021 17:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Sep 2021 17:40:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047b8662a09fdfa7dea8086cf9e2a632d09dd8f2848de9a500d15ae3c2bf7a9`  
		Last Modified: Fri, 24 Sep 2021 17:41:28 GMT  
		Size: 4.4 MB (4449294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84477e5068504078a4d643a66ae31db7aead8076162df1016404ea7f6ec479f9`  
		Last Modified: Fri, 24 Sep 2021 17:41:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c94a831ef4c3b67a6834a3a36c58f4d6c60d52de703d7780d6d7ef071673bd`  
		Last Modified: Fri, 24 Sep 2021 17:41:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
