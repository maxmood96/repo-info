## `nats:2-alpine`

```console
$ docker pull nats@sha256:d54adc86b633899afba362b2d9b8e73118b55722bdd9f5607851e50640e6f6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a7467b5cdca8718a89da4dbc9c6fe1c1b0e808e408a25ae4d79eddd2c82d24e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9785688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375603aac64a03bb6d9f3dc0b93035d1e4251ac412bcec46abf4365c0113d9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 17:20:07 GMT
ENV NATS_SERVER=2.10.18
# Wed, 17 Jul 2024 17:20:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 17 Jul 2024 17:20:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 17 Jul 2024 17:20:10 GMT
EXPOSE 4222 6222 8222
# Wed, 17 Jul 2024 17:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jul 2024 17:20:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfed2c5394f55f420233447be9ecab4c6ee993bb71fc7070cc42966cac1e0e`  
		Last Modified: Wed, 17 Jul 2024 17:20:44 GMT  
		Size: 6.2 MB (6160866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb410539360ea0b98f0354ca52cf97ddbd2e740fe5411087e1160a09ee7b1bb`  
		Last Modified: Wed, 17 Jul 2024 17:20:43 GMT  
		Size: 563.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7e78fd6306a5ee1886413d52529d3ad2030d18f5c10de20e5a678f45036a0`  
		Last Modified: Wed, 17 Jul 2024 17:20:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:874e21de53f9f412c83c2d3985b951a619b30b7cd040644700703a92772ab9e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9200943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49205fdaf2a98247a4369c3581a5505a67c2ca095e96bd375220187ffc1840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:11:22 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:11:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:11:26 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:11:26 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:11:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da4323347517de7f364da317b331e55489fa17bd5d9deb17a0a4453291b541`  
		Last Modified: Mon, 22 Jul 2024 22:11:58 GMT  
		Size: 5.8 MB (5834782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4244560c1b65829997333ab1ed1df1b830cd06fa476593f75a4b8e817605019`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f46f713a94a109b10c1efc57f2953fbc0f7f9d4b749f628080227d8b07b320`  
		Last Modified: Mon, 22 Jul 2024 22:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:213bbaf67033c65c56c1058f48395a59c8884a23789996d4f46b72e9e3e43d53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacedcb9f898b3eebea76a9c833aece4e81cf8131a1d4f60a2a2508f5682866b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:21:38 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:21:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:21:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:21:42 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:21:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6669754ca909beac778774d7643de147c0a48033780bb3e06a57d59c2e7136c`  
		Last Modified: Mon, 22 Jul 2024 22:22:31 GMT  
		Size: 5.8 MB (5826141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40cdcaef7f9f29b1e08c7bf4a83173b8204be369289d1d04b773da36da4262`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d75a871189ea3b9d292b44fe11a01ca199158d55c9183863f29e939a3d0766`  
		Last Modified: Mon, 22 Jul 2024 22:22:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fabaa0067dc4eea075d80ed11b76959c4b94e0ef3a967e25f86b03e5d31b56e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9819841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5176ca202c273c7fa760a1cb1f5dd29c97dcc421bf047a74b97cbe91c61ec2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:25:36 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 23:25:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 23:25:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 23:25:39 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 23:25:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 23:25:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b9d56c3a550077d93d155bd521e641a3191e5f3caf29bf49221b0ef66c26d`  
		Last Modified: Mon, 22 Jul 2024 23:26:10 GMT  
		Size: 5.7 MB (5731935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f006108a88ed1936fe000f4d201711267c67effc483d1a4be48aa0ddae7bc3`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250786191ab0f11e735b0fce167aaaf7d0b1cfdfb4329f68451ce16aa4c8c2bb`  
		Last Modified: Mon, 22 Jul 2024 23:26:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:07190ad1490628071bf257d369dcf8eff092799ab5f584a7c5287a282de4a7ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9274612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e6d0915854268c8f646c4d7bf80e54bd0652a0a09ebce09adf0ff89e2a7d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:53:28 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 21:53:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 21:53:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 21:53:33 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 21:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 21:53:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a23f5ef1d2ac161da343a324b129bfd323feb2bd1b1514c98f5385903a320b`  
		Last Modified: Mon, 22 Jul 2024 21:53:58 GMT  
		Size: 5.7 MB (5702086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034281e5589837e71695fe468a3af82f1d07e3bbe9eeb77a85871cc60cab81d4`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168d160fa3e67bd11ed6992894df816c7f61009da36f66605f38cb65be2dded3`  
		Last Modified: Mon, 22 Jul 2024 21:53:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:97a04efb8e16b07a9ef31fb5e50f1156bf93166628a621644ff9952e5711698e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9487603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f344d23deabe5546323940ae43e072d812444e7c1e9e121b55d0ece35f5afb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:29:39 GMT
ENV NATS_SERVER=2.10.18
# Mon, 22 Jul 2024 22:29:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3f026443e902a21e787382ca10e1446bf02a8bb779224b1b7b33ea6483f76b02' ;; 		armhf) natsArch='arm6'; sha256='69bc51de3e7c4f2585c68a51372f0b0e4fbc4048d9251606480dd0f416f28f87' ;; 		armv7) natsArch='arm7'; sha256='80b7ba618d76f22b79bc192a4867c799e9c02fae10f8938d4514a3954f791174' ;; 		x86_64) natsArch='amd64'; sha256='7760fe7347ba8e8daf4474811cf7fc301713aa8f3d4e0787d3e79a496dd537b2' ;; 		x86) natsArch='386'; sha256='2e7cb64dd7f0de0256d74a2ea3792c63c3af28cddc66ce7101f1156e40941c56' ;; 		s390x) natsArch='s390x'; sha256='c9534f9d4c6783780e71e61037890fcb4dda3917c875e904209aef3b7b5e74b0' ;; 		ppc64le) natsArch='ppc64le'; sha256='f6020a31d6fc3923b1782eb22f6f16e27f4e0c0a004ce8d014d7298c9a3a3082' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 22 Jul 2024 22:29:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 22 Jul 2024 22:29:47 GMT
EXPOSE 4222 6222 8222
# Mon, 22 Jul 2024 22:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:29:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfd2ac3203a8dcedf98f2b34f3ebdc01f6d589b8b4af3fce188d548c373defa`  
		Last Modified: Mon, 22 Jul 2024 22:30:18 GMT  
		Size: 6.0 MB (6025560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21cbf2b27238289e050f352d99c5cccc993d1fc47011bd5ced05786e3d900ce`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 564.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a8290432354451c68923c535f0b0fd17195d8fb26f35b6f1d69566b3d29990`  
		Last Modified: Mon, 22 Jul 2024 22:30:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
