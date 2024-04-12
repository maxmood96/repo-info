## `nats:alpine`

```console
$ docker pull nats@sha256:81f36bfe9dfef7cd3768abaf55fc309123cf6bf1cb0d8305a6700ff36034b93b
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
$ docker pull nats@sha256:6fb38aaa7467fc0f95b9b8b82667e13a6ab33e88328266114cd5972fd4ce7a36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9593547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed50fb89a515fd8a7ac65959ec5c4447b3224af721405ffb59482b5edcf8b7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:04:51 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:04:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:04:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:04:54 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:04:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b83a0e28b2579e281f6a89215c7220be68fd968d6f29a63794abbc28c1264`  
		Last Modified: Fri, 12 Apr 2024 01:05:34 GMT  
		Size: 6.2 MB (6183818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31291d77521460d7df0a79503a8b9457e85667ae9d4fc313a127f66b5bbee6`  
		Last Modified: Fri, 12 Apr 2024 01:05:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287ee2a0c75e9620dfa28523cdd568ab557a6356d4696dff7d6053cb24ddc57e`  
		Last Modified: Fri, 12 Apr 2024 01:05:33 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4c0708f1a1f3e72f0ef54f943c89664e0e33ada46d4570059f9b030706fd075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9065103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddbf631edf0b613a3d945ef358ae897923e2efe2c79b039656d4b8d47860ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 00:22:48 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 00:22:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 00:22:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 00:22:51 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 00:22:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c7d0d4700c33110f1ac7087fa2e367a586f182ba402cb61f74ae92d6fe8b8`  
		Last Modified: Fri, 12 Apr 2024 00:23:27 GMT  
		Size: 5.9 MB (5898707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21706ec26a9583471f36cc02a6766a1e50bbe92db3f9a98ceeea4dac4445bc25`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f147485e678690dd524f4b159e6e077457750746794ab2255915b53f3bd1dd1`  
		Last Modified: Fri, 12 Apr 2024 00:23:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ade8887bc9138200b1f580e7036361bd80cd3027068af2a2664e67bbbc57904b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8811114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ad3b5bf2ebda9cb467a425e00b1300b0d9769c3a509b2649a783944563b47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 02:09:16 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 02:09:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 02:09:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 02:09:19 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 02:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 02:09:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32728fd54d4b99d4f64b2dab6bf27035f311e84edaa92b774ea49d4800b00a9`  
		Last Modified: Fri, 12 Apr 2024 02:10:07 GMT  
		Size: 5.9 MB (5891216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46b81b27e51ba18c9118802ee6fe4869bf644b5586c6d1a21d2d91608b24d2`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f130b5e6b2c0ebba754acdb92f3183b738c23973b3db0b94e59b853dc32aa91`  
		Last Modified: Fri, 12 Apr 2024 02:10:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:54227510dab6ce16b9505e2d7d9623172a56b458e7cf6fa093352856fdaf1dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6832ccc64bfe3952877036dfadb9b2b74cd8eb60d251a8b6e6b605f5d33c0422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 01:16:39 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 01:16:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 01:16:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 01:16:41 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 01:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 01:16:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e5f48f33465893e7a03da432d74d140b6d2cea0553713978aebfd63f8c0265`  
		Last Modified: Fri, 12 Apr 2024 01:17:38 GMT  
		Size: 5.8 MB (5755465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89d0dcff8ed4386bb0881b5769919ce56fff66d31d80ec103a2e03bd10a425`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d251a03c85ddc7482b8a46395e8613935a023570eb2f4f099b6182dea113628`  
		Last Modified: Fri, 12 Apr 2024 01:17:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:3fa5e73c7e24e8f1e43e3ecd494ce7f32cbfadc655f4660ce280a48ac52d1451
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9093333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875b9062cfc74a350c9d2388c57224a5c6031da73e762a5b19053ac9bd7cfef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Apr 2024 23:28:08 GMT
ENV NATS_SERVER=2.10.14
# Thu, 11 Apr 2024 23:28:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Apr 2024 23:28:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Apr 2024 23:28:14 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Apr 2024 23:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Apr 2024 23:28:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b4ac8899f3637d524bf1ee551512ff20ae40aad42a90a94b61fad821e6c5f`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 5.7 MB (5733983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f2c2746ccb98de39771ca529912077bda13a11dd53009e3ac1d242127ccdff`  
		Last Modified: Thu, 11 Apr 2024 23:29:08 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ade4254b67d2f2d84169d2a6b63a03abedba8492175281cdb7ddf1f7bb1de30`  
		Last Modified: Thu, 11 Apr 2024 23:29:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:ba9c59eddc65513d080f04f09947c52baffc47d109303b7075702302336f38b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9309748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d457d7796f169712a9f6882af4a12b292e8604b796f6d4dba36a4874fd15b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Apr 2024 06:30:34 GMT
ENV NATS_SERVER=2.10.14
# Fri, 12 Apr 2024 06:30:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='57aa4464759d211df247b645dae6d0c0724d84aa2db3dc042cd2dc9fe8553302' ;; 		armhf) natsArch='arm6'; sha256='125dba652ee7c4c60bf1af3ced1c590e7d32f7624e27364c278069da660f04ea' ;; 		armv7) natsArch='arm7'; sha256='1215a787ac52d03bc2c43069ac4229b891be7dafeb2ea44f58dc5c854001629c' ;; 		x86_64) natsArch='amd64'; sha256='8e1ba988220e7f3a0156c085b7c4fe47222ee8342cf1cfa7b364e30d9d6aa47d' ;; 		x86) natsArch='386'; sha256='29b361db7d0ece5ba74ac6aa1911446573db3a4806c175df4bd37142bccf5e06' ;; 		s390x) natsArch='s390x'; sha256='f9a3c2b1ca2d89bc865b08d37451e5c1949112e042c69fdb88bbb6938ad774a8' ;; 		ppc64le) natsArch='ppc64le'; sha256='276f4f5d080a96c31c4e1a15e84aafefef5d82dd93c112ea659f17f068ab4b6a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 12 Apr 2024 06:30:36 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 12 Apr 2024 06:30:36 GMT
EXPOSE 4222 6222 8222
# Fri, 12 Apr 2024 06:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Apr 2024 06:30:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ae05130d854f39c316dac2eb030cf0e91d97cdf03dfcd2941d9f752cd759f2`  
		Last Modified: Fri, 12 Apr 2024 06:33:03 GMT  
		Size: 6.1 MB (6066114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9345be0cde84fd2c9912c2c600e22ed40dbb1003213252dbbe9b8cf7023e64e9`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff8e384b7de86ae73e733bf01e2e479520a72415bd283f554fd635e4a1318cc`  
		Last Modified: Fri, 12 Apr 2024 06:33:02 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
