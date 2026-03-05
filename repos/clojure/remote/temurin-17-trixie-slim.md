## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:ba8702a1efbdc2088e8a7a2b57b34d8c81c79eef5c8e07a7cb47fd4002c36c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dcaf929dcb72e4e4ae2101d028f55878498f964bdd2a2218079ead031c5a1c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247423393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf62206182aba95c10b70f2d9e74003493eb8b6d1a79126167f0d5e200e0291`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:24 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:24 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e988cd6f41e2d66b063d57a8a5be28d78eb56408954353c2621eff6379e3ca6`  
		Last Modified: Wed, 04 Mar 2026 17:51:04 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c31781c16cab39f1b9adb4be5562ccf4d735337f2b42b6826f8a5ed62cd272`  
		Last Modified: Wed, 04 Mar 2026 17:51:02 GMT  
		Size: 72.0 MB (72015011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8446a2cd9e80561c212b25cddf1cd7ba3122de1dded8a8c61a46b8f841f377b7`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4fd80cc20b3654b74eb6d5b446a0690a6ebb0070357f1bd3f804f1aa9b0712`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc25e7c1d7ae76250d98f66fca1fb1279c5c1a80d5f2cb3b6686aea73edb7147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6b1271f88a4ceddc4991b04e5abf56adaa886002c573fd92b2ed6185abd960`

```dockerfile
```

-	Layers:
	-	`sha256:bf633e8cc889f224b5938c942966c7867a52d926fe7fe0bd51bfd0366d967846`  
		Last Modified: Wed, 04 Mar 2026 17:51:00 GMT  
		Size: 5.3 MB (5259064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce3369f4736f9eb2a48f09c901c05cd29591685d25d37fcb836960fa1723ece9`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:deb07092beefa2fb718c9c263804adde0f1c4ef406e711442a741a8a70154ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246409069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de8b00c8dc50d83383383b90a92d7e524a4cd3b5127f982481a1651673ea16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:51 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:51 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800d149157ba726af18b512e9b2707caa37e4b3ecdee927ec0150a8b00403d9b`  
		Last Modified: Wed, 04 Mar 2026 17:50:31 GMT  
		Size: 144.4 MB (144436183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3735c335032e048f436720b3abba5cfb58ac6560a8de587be06a636bf517af8f`  
		Last Modified: Wed, 04 Mar 2026 17:50:30 GMT  
		Size: 71.8 MB (71831745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50d27a5051a42f0d8b0f5f896be78fcd3c9ad369e94828975523f9c6d4dc943`  
		Last Modified: Wed, 04 Mar 2026 17:50:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4b7f3e180dd4b707db2154a39987aeec403595098b018a05e09fe496a80fd`  
		Last Modified: Wed, 04 Mar 2026 17:50:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8737711d549cff62c27c515729e70f2f22cc881e18a9555283c5a7fd4b8a8a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ab2273f393b6292aee7f3fde78e35b61a44753e26d4f924ad76d847a8cdc2`

```dockerfile
```

-	Layers:
	-	`sha256:1fa36fcbe9549adea1bcacd7778fc46a75259281282c0a7f50bed518544b22e5`  
		Last Modified: Wed, 04 Mar 2026 17:50:27 GMT  
		Size: 5.3 MB (5264833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc34b63de74426dcb2a843a95e6d999a8070d19fb40b4335e5f7fe756b7a684a`  
		Last Modified: Wed, 04 Mar 2026 17:50:27 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d85d4d9f15f031c53f936de4ef1097711f390de90d9ee9abc3b22bae8f34c0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256467439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a06101cec26dfa403ca67291d465ffa4f25f4d92a22535112ddb158a17671e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 18:01:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:01:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:01:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:01:26 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:01:27 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:02:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:02:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:02:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:02:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:02:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9ded9d8155278a982468967c97224cc4928146d30246672ff1794621996185`  
		Last Modified: Wed, 04 Mar 2026 18:02:56 GMT  
		Size: 145.4 MB (145438221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cc9e78af650fd05f053e65985c83b4ee1e8cab94c408a7fc22ade666dee09e`  
		Last Modified: Wed, 04 Mar 2026 18:02:55 GMT  
		Size: 77.4 MB (77427957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba090cd412c9579516293f2e36ef44a4e86fa11fe180ca1fb07dfe53493f000`  
		Last Modified: Wed, 04 Mar 2026 18:02:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebad03eed716b588160c8c11107a399b88a894904e6ff8c232484a045b2623f4`  
		Last Modified: Wed, 04 Mar 2026 18:02:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfb23c5f9616c46e02ac138e3da546b2b49d74bbde9a4431d88af67d2f8cf500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a831490764a85b097c627fc0ef9d19a3399ffd22af156b8473038af2f8536b7`

```dockerfile
```

-	Layers:
	-	`sha256:1a060a12fe8eaded2077108d54d664862dfb8ac1bcccf7ee93dd6c98bf6a2f84`  
		Last Modified: Wed, 04 Mar 2026 18:02:51 GMT  
		Size: 5.3 MB (5263435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2576ecbb3bb5bfa7b469149c589d91a09bb1f9daf2d47d6675d4615d9bb4680c`  
		Last Modified: Wed, 04 Mar 2026 18:02:51 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:75082c3ecc9df4c708bcb39b6a1b31ea47ff728fc1cac12ee4efd55e531db7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241839662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03cfb1de5cd961f6c7f5368b6c9fd5248ee6f8717e359a16053761460d9d2904`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:00:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:00:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:00:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:00:22 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 11:00:22 GMT
WORKDIR /tmp
# Thu, 05 Mar 2026 06:24:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Mar 2026 06:24:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Mar 2026 06:24:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Mar 2026 06:24:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Mar 2026 06:24:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c563a7e83c0073076553db10b62cc19d4a3173b8d64e403513851f43436892cd`  
		Last Modified: Wed, 04 Mar 2026 11:07:48 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170367c3078b5c5361489f207887eff764c1fc325ba814a14a733d2469c029f9`  
		Last Modified: Thu, 05 Mar 2026 06:27:50 GMT  
		Size: 70.9 MB (70899204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23e1cd0bd8c86eac106a649b342856a46cd6774cef2b14ad47192e64a498085`  
		Last Modified: Thu, 05 Mar 2026 06:27:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018bbfce2f3b0adc8db8b07cd035f3ebd7b8ed7b18f0e1b7d270ad3b698ef981`  
		Last Modified: Thu, 05 Mar 2026 06:27:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12f87a1b4238ef24ed333076fc4d6a1405d7c238f93bcebf161cc2cb57768193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3512208095eaa16422d0be1c0d1785c37796b0c8fb92a7cae05ecb73d4f3dd7a`

```dockerfile
```

-	Layers:
	-	`sha256:4b7e09dc7af5dc331995df43a81376ad9ff86e9e0157350afe1d2c780897a9d6`  
		Last Modified: Thu, 05 Mar 2026 06:27:40 GMT  
		Size: 5.2 MB (5246609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fcd7b0d5e30a5da49fbf51654a1ff76e4f353df0bf6433883e3c9e8861ce89`  
		Last Modified: Thu, 05 Mar 2026 06:27:39 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9b7cc78e38ab39f8279a75958784a79c1f279b6fc359fa59beb28a6e6c20e735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238449941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135b009fa24b7f8cbf38a261cc1f5ae32c7ae1fbd37bf77c5a28fb93301fce27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:50:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:06 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:06 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae00c4bd64aa1255d2aed8144307a0126335967f1c1c453bc256c936f95a44d`  
		Last Modified: Wed, 04 Mar 2026 17:50:49 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80224e2c5b7369a2fa529474454938b60241f8f74aa81b3a41d975dfce2da203`  
		Last Modified: Wed, 04 Mar 2026 17:50:48 GMT  
		Size: 73.0 MB (72983606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e590fb5c705c8cb64eb4cf7de0d456f6e151093a6c732dc5a48fc2c06abab`  
		Last Modified: Wed, 04 Mar 2026 17:50:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a22f9718e89b4dd1cb4f0e7b058f96247b156956b526c39e8b4f6398df49a`  
		Last Modified: Wed, 04 Mar 2026 17:50:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff97964cbe3fd6dfdb682235ab3e851315408847e3794ea97fe22d8307e761aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b8de41dc21944ef90bdcf022ab8827656004c73272a3afea612ac29f96ecaa`

```dockerfile
```

-	Layers:
	-	`sha256:b37d8db5a269c05cd16f89549cb70b4974136b80360c30a250d5df22e9bef88c`  
		Last Modified: Wed, 04 Mar 2026 17:50:46 GMT  
		Size: 5.3 MB (5254988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b84dec08b8455e9778b0077dff750b90982812bf182e6c069d349d9a62657ac`  
		Last Modified: Wed, 04 Mar 2026 17:50:46 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
