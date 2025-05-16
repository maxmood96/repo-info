## `nats:2-alpine`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 15 May 2025 20:40:04 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 15 May 2025 20:33:28 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 15 May 2025 20:35:59 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 15 May 2025 20:25:28 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json
