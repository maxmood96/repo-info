## `nats:2-alpine`

```console
$ docker pull nats@sha256:b68bf17c8921ab07d1307206c57d3a073c5afddd7a4de5c13e8dae5b28926a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:65866b6c1aba8acafa981d67d5a192661eac2450a76aaa17b26723181e706d37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b1a28231be8afbb5398cb97ffc1c7c6d5ff92f93e0b8112f46a33190f303f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Mon, 12 Sep 2022 19:31:42 GMT
ENV NATS_SERVER=2.9.0
# Mon, 12 Sep 2022 19:31:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b82c2910819bbf9350a5040ba2145b5e17d0faf8fca502505a4845ce1dcba441' ;; 		armhf) natsArch='arm6'; sha256='4f5f02bd8e06e83d685f7cba76620ae76cdfb7bd94f89e3aea323bbd0bf6ab3b' ;; 		armv7) natsArch='arm7'; sha256='0af9e816fb4a47274d2f7b1d1ebebd13568f0b70d466feefdd04cf1f14a0195f' ;; 		x86_64) natsArch='amd64'; sha256='e2c678de6900dfd126ce181a1103201ac6fb4e63f7112d320932a011db64d4e0' ;; 		x86) natsArch='386'; sha256='a617f94da82e2518549d2192d336be1da09674498553d117a95e167c4f3425ca' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 12 Sep 2022 19:31:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 12 Sep 2022 19:31:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 12 Sep 2022 19:31:45 GMT
EXPOSE 4222 6222 8222
# Mon, 12 Sep 2022 19:31:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 19:31:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea240cdc5587948c840053f07c13be99688645429983c0e761059967ed9ea8c5`  
		Last Modified: Mon, 12 Sep 2022 19:32:49 GMT  
		Size: 5.2 MB (5187250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3491be0cc4877aa61624c7aacc64065db9b2ab1e311fec95ffd8bb2845496a`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29584c3b600243845e3a795968d4ab77f0c31fe91068243b9e981bebdf5244f`  
		Last Modified: Mon, 12 Sep 2022 19:32:48 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b504cbebb7c50f895757baff017068b257eb61fe616bfbe3f1126f0ea8f79b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7567285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896d9025c4bbee5c740d89fe2a51646ca3334aa2aff3aff3aca438884c1e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:49:20 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:49:23 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:49:23 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:49:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e8870dd29b9e9ffabdfc8cd768667a77c65e9e338bf8569257854740fdf82b`  
		Last Modified: Thu, 22 Sep 2022 23:50:30 GMT  
		Size: 5.0 MB (4952317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c589ba81c8b7920719ac20578d279e73e40a37f3bd0e5743a390a5f1a5f0899`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a764dcbb9fff9d114779f0310c6a8a3f8f2bda031f16ed9302173aae8f4cc7d`  
		Last Modified: Thu, 22 Sep 2022 23:50:29 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43a4795e7153c524620b43f9cf744659f5f32f1eb37326b2259be4f06dc7a959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eadfdcca40f49ba08c9b57db4711db2b88b1027405154bb190abd16686cc4c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:57:45 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:57:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:57:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:57:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:57:48 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:57:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28148b83a7e0626bede5387abe8640718cde573f4e7e2fc013b181c07a8b21a`  
		Last Modified: Thu, 22 Sep 2022 23:59:04 GMT  
		Size: 4.9 MB (4949037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb4b374b15114a9cee11f09286b893ca3cc79d82fab81fb81921ca5969142ae`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704470fff25768fb506edddc3efac7a081fbeb8c379a243a84a60554c121062e`  
		Last Modified: Thu, 22 Sep 2022 23:59:03 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af501466b5b4748dd58d6a01314dc8b52929cc19ede83b48599b301569f1cfc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f52297bec9c9125da3427bf806b078a28bc0afc58dcf442110dc6f5455c18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 22 Sep 2022 23:40:04 GMT
ENV NATS_SERVER=2.9.1
# Thu, 22 Sep 2022 23:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='d0aa00133c68e3dd1c791272fe352ba5d5ec097c58991946c5a0e66e06fdca4c' ;; 		armhf) natsArch='arm6'; sha256='794267eb36c86034b8f800fda1a60019538ac79788ca3e060cbe737dcbe6e8b8' ;; 		armv7) natsArch='arm7'; sha256='22c9d0304daf83d8ed08431121f4e389954ea9447c39b407d07eee588ac31dc5' ;; 		x86_64) natsArch='amd64'; sha256='7d2d6a245f3c42b0ac5a75a6cf345235bef534a0baeabeb374b328e08b60a25b' ;; 		x86) natsArch='386'; sha256='f63cbffde08a8c6716a1dba464a52df48265186e8b0386a4815e7c549143599a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 22 Sep 2022 23:40:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 22 Sep 2022 23:40:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 22 Sep 2022 23:40:09 GMT
EXPOSE 4222 6222 8222
# Thu, 22 Sep 2022 23:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 23:40:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08937f059ddd40b2696cabb3fc09473c8f136f25a55e1818bd8cd11177bb5b0`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 4.8 MB (4775257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8b44164b339cf12c411012651587f34f3451b6c3161b0f6c18d64d2a28d84a`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a983c21365eff677a992cc5781a1ae47afd965f00abe6bd59ee79649c0c13`  
		Last Modified: Thu, 22 Sep 2022 23:41:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
