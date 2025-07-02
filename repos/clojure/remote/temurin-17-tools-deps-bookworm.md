## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:d6d3edbe5731553b49cdf4d2ec12d541e8b6b52f5fba6096e2e92d36db83ad6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cc4dc857334e8eda110c3ccb16266f2259d784ed8e295dcdb5ee74fd231221e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274123397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95578848b936fb42325d6b18d1375f2c5c4a5caf3898f857b1484c4f68cd4fe2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed96396b24255cadce6240e231e31609b7786c8502dcb580469b7f35d24c158f`  
		Last Modified: Wed, 02 Jul 2025 13:38:44 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e78d23a46ad5bb920dcb7c1a0b5b4a8cc9e45e0c93e9a1ae595658fcb2974ad`  
		Last Modified: Wed, 02 Jul 2025 04:17:10 GMT  
		Size: 81.0 MB (80993045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02e5a593723dcfdba0dfcb30ba03c104622162174856c375bd57a19286b63df`  
		Last Modified: Wed, 02 Jul 2025 11:52:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca5d0b66bd0015dcad9f87ce1a4572a16c9849adbe9067789deabe0cad45f0`  
		Last Modified: Wed, 02 Jul 2025 11:52:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f53afc3be49edd7876eaff0c601edcd24405a94053427dbd2066f4023f4866c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7384089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87de1b8a9839eb609ecb4fc39464e123c7c0ccfdaa63e857122b146fd4822ce3`

```dockerfile
```

-	Layers:
	-	`sha256:ac14263d97e629de7fdcb1c2cda39467eab781fce7357e3f3153ed00f51bd88a`  
		Last Modified: Wed, 02 Jul 2025 06:37:10 GMT  
		Size: 7.4 MB (7368268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baff5dc9c93a40a5396fdce4ed0d68918fc1a4e4d216df9cba28866b4dc5ab73`  
		Last Modified: Wed, 02 Jul 2025 06:37:11 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:33504014256a7afe238eae533985ad011a63386d81b9eacff0ec248394d4b0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272704597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2780474bf5e4dc6240ced70e4cf125740d0f131c5650d8c8961f7683f139c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5395bb37fe55c207b5411c35f7f67775714da2a361b6917505a8ed8fce264e4`  
		Last Modified: Wed, 02 Jul 2025 12:29:19 GMT  
		Size: 143.5 MB (143512649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f865e646bef597b3b2706346468108ea9d5c9acaa4afcdd4141e0149d25c9e77`  
		Last Modified: Wed, 02 Jul 2025 12:36:15 GMT  
		Size: 80.9 MB (80852122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1f48126098e6bb0fdb53e8206fb19c14683bcd50692829db365f907b5e3971`  
		Last Modified: Wed, 02 Jul 2025 12:36:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c603995edf24a309bbcd7a5aed2fae21ec9858a627214cd8b8b5d2bcfa850b`  
		Last Modified: Wed, 02 Jul 2025 12:36:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:44bdbc6880df87fdc4da2d96cb059c2dd7634e471ee87973635548d5054e727a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d3c59195f6d4bf379aa0154306fd6ba5633b0147bc83d957b67561d04e3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:f5d977e9dde90ba59baead75ec71887fff87b24cd3ca11fbf9a9f6eb1578d4af`  
		Last Modified: Wed, 02 Jul 2025 15:37:15 GMT  
		Size: 7.4 MB (7374031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7aca9db4faf2ed8bfddcaaac1b2e894eb9833b4fe3514f87208909da0061de`  
		Last Modified: Wed, 02 Jul 2025 15:37:16 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8c27640a88dd1b7265e11c67c97757617d5e76f0d24d43b21fd0eb76f9362629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283437882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25164f392b27026591d7dc913e47db476bed6bb26c5f60b6baea2fa674fe159`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3838865167232f93563bc8b7c511ca0ccc537b5974d36b8a7fd010a7890faf35`  
		Last Modified: Wed, 02 Jul 2025 13:38:29 GMT  
		Size: 144.3 MB (144280276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dae324777e7ab6545fd8763facad4988d6396d543ee0cac9ec1c59b851012a`  
		Last Modified: Wed, 02 Jul 2025 13:38:44 GMT  
		Size: 86.8 MB (86819324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7308c62e33b091bef1f18e807af251a67643bae8f5115f1278ab46862598b2e8`  
		Last Modified: Wed, 02 Jul 2025 10:36:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71a32bf5a38fc50edabc4950f0b4c2069a7c7c42bd4b04b8c758e053bb44095`  
		Last Modified: Wed, 02 Jul 2025 10:36:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c7471ee3704b7049eb831997e77929278fba6361bc9d467ff42d70b1adc4eba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8244ff37b9507dd4ba40033cdd6f44100c239b2b91d013c745ca46f79478e0a4`

```dockerfile
```

-	Layers:
	-	`sha256:30bd4d3e1f09ae74970a814517353b7f112cf20672af4c865cbbc8a6150b0400`  
		Last Modified: Wed, 02 Jul 2025 12:37:00 GMT  
		Size: 7.4 MB (7373472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6f4c8d8ed96bc2fc1ab2b63574fc578dc651f0e5f59554f7311aea03aa200f`  
		Last Modified: Wed, 02 Jul 2025 12:37:01 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a7fcf22665154de43c016ad69d6fc8016ee755b4b65f35844b66f1ddbbf06996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261623309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c33a9b3149c52d14489fb3e2046174948863c44d61e3db88adc514453ddb793`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeee636da6e73425d7e3dbb4251d5d573a52673a2bf470e0ed3437c5331886f`  
		Last Modified: Wed, 02 Jul 2025 06:34:41 GMT  
		Size: 134.7 MB (134673586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c7823a7f2ec934ef745deb3023b2da7ca6b8f274b5a410a6e666c4e73bbab9`  
		Last Modified: Wed, 02 Jul 2025 06:40:18 GMT  
		Size: 79.8 MB (79799397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08254cf3c33dc6e967e2da755abb0e40312a50f59e4cb01287a9ebbd6c298ed`  
		Last Modified: Wed, 02 Jul 2025 06:40:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5a9ce0f4af14ddfe33f74d2d3a9c8a66fc9c736c406d2581be9bf009a49fc2`  
		Last Modified: Wed, 02 Jul 2025 06:40:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c1f26e68d3438657cdd3e7ba5e75880234f1b7ef1cd7742e8b36f60bbb258e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69d1d609e2e9eabe72367765fe4825ce7d949af45e8958d8ef29c4a707c42b6`

```dockerfile
```

-	Layers:
	-	`sha256:cf59fc96bf8f30a61aecdf4fa31d2a84a7fcd3819b7aab36d88fff99597d49a7`  
		Last Modified: Wed, 02 Jul 2025 09:36:51 GMT  
		Size: 7.4 MB (7359587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160557580acc81640344ce839b67c7ca636a7cb6a2a0496c0f881aa9dd61f810`  
		Last Modified: Wed, 02 Jul 2025 09:36:52 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
