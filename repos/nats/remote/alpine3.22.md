## `nats:alpine3.22`

```console
$ docker pull nats@sha256:b8d6a01568a7837d5186f948a3ebfae1bdf5a602268273b50704655982596b22
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
$ docker pull nats@sha256:69435fcc1356278c35dde2a3b3d9f2c4504f57b921d38612d36200a9c7b51067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10580056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e96d11240320c8d079058907e6b1a349c3c164f6d1057c7d4141b67803ef0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:50be8340a33b28b7069d77e81278e1150e46e62e5739a5ef524f3b10b6315d93`  
		Last Modified: Tue, 03 Jun 2025 18:08:18 GMT  
		Size: 6.8 MB (6782240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0d77f12e11abe2cbbe9f81a2abb732a2dea9eaf80743c4fa1d667fa5788ec`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41e063c3ba2c3d1eacaaddf312305350fd53db659416972db737157b54fb5c`  
		Last Modified: Tue, 03 Jun 2025 18:08:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:770fc5b17c3e852bea98835c4f770de25350891225d2d5c48a17079cd2a87f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece4f13433515ab3468766d0750908f38501255daea31da2aab9466abd8dd13`

```dockerfile
```

-	Layers:
	-	`sha256:993a3e77289857e49dcc0d82e8b0a4d01bf97fc1ac52f27adc1b6d9f46be3010`  
		Last Modified: Tue, 03 Jun 2025 20:56:48 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:cc02d2d98d5248ae02ac731a42436bcf7c257a2336cb6ccc18c0a0d33aca7425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10002162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7ffccb3eb9188263f6e9ee5ff6be0d88a00817e7d4a7a880ef153ff6b59861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:ee3cdfa139575e7698957b4ff36ff5e3b9c98dcca74e89a001ef2062de4433d8`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 6.5 MB (6500264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3195bedba82c8298239740a21ea08ee0b417d4c68b4eb96b52ad6c083c2c920`  
		Last Modified: Tue, 03 Jun 2025 17:57:02 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93998e0b8d5c431d6f762091f25cb87996747747bf0554bc73c73a2f31e190`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd850c5ec391a375d438c70b5cc24af732269f5631ab424afdb6f809d708e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1f72e1e723af723f70095a15f2853df338bcc41fbb18fb2f275a71cf0c8c37`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8dba6556e09db91573b8694623b3159599ceb566967dd357bf582cfdc908c`  
		Last Modified: Tue, 03 Jun 2025 20:56:52 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bd62d7bcee4a2e2d4e3fe84830bbd978a3027b81e7976b723cfce5c113824abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9708379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efdf790e38279933f555c5ef6b82e2fb30e6d8eb6e85274bb375c1c88aced7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:01c4277d4cc00a376afb142f8ea748e710d48f75eddcf7a2510c5a1e088857e2`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 6.5 MB (6488230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e94ae1fb6404d5eb4989cef0cc09a96573006b7bd7d4e7f7fbab996b9ce90c`  
		Last Modified: Tue, 03 Jun 2025 17:57:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f107f5a32f8d0ab9f4a4a7746509690c6c4845a952c7df17aa5b2e4bc6e7a3`  
		Last Modified: Tue, 03 Jun 2025 17:57:04 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:3191c0cbc6ea566ab41e82bdcfd3a1bcfe0757dc82b606a411fdb61d50858d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3fb67fa07d336d64e774f94f1074d759291d6e8b14b2b24d0c144e3a1ea07`

```dockerfile
```

-	Layers:
	-	`sha256:52a7538138245df9dcdc747a5c3e46f172218df3092764925fdbc21fb2a58298`  
		Last Modified: Tue, 03 Jun 2025 20:56:55 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5dd5eb415f3c3b50eb6e637d9eab8c4ec5726e575550f46a0853226a8da6edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae7761a85b9922c5be272284ee27fe32bfd3b1a78d3239e429792033c7ced6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:6826d2797f1cf0f48d78d168877a33ef918811eaa7ee6146a8653f4218cf6e56`  
		Last Modified: Tue, 03 Jun 2025 18:23:10 GMT  
		Size: 6.3 MB (6271484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2ec423b14754303830aaf58d608bc667aab81252f2b170550982a6c4aee78`  
		Last Modified: Tue, 03 Jun 2025 18:12:01 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac99aa05c0616d567688e33499eacc91da2b7c79dd4b91fdc6bc363573dccd4`  
		Last Modified: Tue, 03 Jun 2025 18:12:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f57f8e16b74edcba83577e18c83f6c830b2de03df54acd64a65d88ab4b5f5ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6f8fff81a6020fdbd737e9dd518b019a3b205e35d387235d0339aec5b55092`

```dockerfile
```

-	Layers:
	-	`sha256:c61cb3463dab986b2ecb7f263eea6eff56bfdb0d4075df19122df210a8d0a062`  
		Last Modified: Tue, 03 Jun 2025 20:56:59 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:04f768ca98d273ca56dc14213654250fb52045b383bce5db0e58444c23697d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ee2cb1b02b4eeb2714421cdd6b2e9f5ba023f8e508c2b604861f33248ccfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:f66500e2c223c5a3f4777f4d7f4ffcec1ca21a34f687704db2a6d0e661fe0299`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 6.3 MB (6254211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198db56aeb51065eb35574df93180297f06ba8d180108a952be65d93fa4e7dd2`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df632b2ea33fceba251c68a32d3efed10d3b495018d7e16d1b256225dd38aef8`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a11e45d5ebc10e2f442f0730348545d2ec0f0645f0f047a39364c6073754d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872e45d8950ac438f1cc639d1fde3610446df42c33be57d2ce16b2eef0e02297`

```dockerfile
```

-	Layers:
	-	`sha256:b2fdd3426bf4664ed50234140c9c5e23667db50fb3545c6a3874643740ef5aaf`  
		Last Modified: Tue, 03 Jun 2025 20:57:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:081db236c5c2d779dcea7087bfea30c8252499477626f616458bb70b78054bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10267911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9772610e623e3eae3e2949e0e470f0755004398628ced20be8fe593671829030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 16:53:31 GMT
ENV NATS_SERVER=2.11.4
# Mon, 02 Jun 2025 16:53:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:32c44dcd57da31d89c4bf6d887262bfc6e7136e1132734822ddb4586096692a0`  
		Last Modified: Tue, 03 Jun 2025 17:57:07 GMT  
		Size: 6.6 MB (6619415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93bad89a83837b6afc8b1128b9f0d132c74ba14e1c7f52f407fbe775cb13a2`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ded513c6eb3a5fff1e0ab2d6ac1560515bbf0389375e4759c71a1b2c0b6e97`  
		Last Modified: Tue, 03 Jun 2025 17:57:08 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b96db90bf17f90a65aaa3a6fa7ea4250df1f9ee0d9d13d52b7d3c8f926242340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e98ba8254d35c0c12076fa3f077b261896b884cb797b2b50e57f1f79bdaa45`

```dockerfile
```

-	Layers:
	-	`sha256:68ad3f417d73aacb9e3e3a8a3fbde0712715fd19f474e71d7f05c3507eeb168b`  
		Last Modified: Tue, 03 Jun 2025 20:57:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json
