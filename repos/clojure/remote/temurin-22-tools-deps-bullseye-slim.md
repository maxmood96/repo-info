## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b77ab76ec1d87e654f163ac9eceb05ea53852c8c8e911b783396b8c3d7e52306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:982b682f20a6ea7b7de86de4c3f439bab7eb9d5b3f650e915cd47ceabd079c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246762907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1a2131414443f9561bf3725c2c6cce0fd599540d040c24216f195e021ba47b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eaa52c3852a126d4541fd5b4ba09945a4720d0b0bcbb56de9018c8565a75b9`  
		Last Modified: Tue, 02 Jul 2024 07:09:32 GMT  
		Size: 156.7 MB (156715504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb26eb0e1164fee66a72c94bbaaab4f0d56fca4b3964edb0c76b02d2d6b59d7`  
		Last Modified: Tue, 02 Jul 2024 07:09:31 GMT  
		Size: 58.6 MB (58624077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a7ecb4ba8aabc0000d54e6935e2d6a3ae55bdffc9a5f4c1c65c7c5b1ff9215`  
		Last Modified: Tue, 02 Jul 2024 07:09:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed4e0cfcfda81e76ffc7da93edb738bf446da54e51a5bf3a4b00d3a9893a4f`  
		Last Modified: Tue, 02 Jul 2024 07:09:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92f0d803d0b3985ad49b142e3a03f9b43d576a0f59644430be2eb9abba180728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a8ae3788bf3f969cb7764b8e7a4c2a29bff366a8364c8c48e9d7b9ba96d8c7`

```dockerfile
```

-	Layers:
	-	`sha256:f1add503f66b1ad93f1ce276727d89932a2678987c3f394e48d006fdf7644455`  
		Last Modified: Tue, 02 Jul 2024 07:09:30 GMT  
		Size: 4.9 MB (4909266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c2b6e647055b9e058dfa6f1086eec2fadb29992abdef3c32c3c8f74708298f0`  
		Last Modified: Tue, 02 Jul 2024 07:09:29 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:540de9c959e64755bceeec201e5e2e7c87769ef86be3453ca1bf303b8d8751ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243552697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9669bf5c4e50f6a4c09990f78cfd64a340eabfc148f106f1929d6d22f78d6130`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7272749026505d79c43a10520a0b6d7e6936c2db39fc18cb0bc9fba1ceeca81c`  
		Last Modified: Tue, 02 Jul 2024 09:46:13 GMT  
		Size: 154.7 MB (154738013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70063c67f6f029080a6dd7ec65d59061eb7a788ae7bcfd47799f99ce356b2961`  
		Last Modified: Tue, 02 Jul 2024 09:49:59 GMT  
		Size: 58.7 MB (58744029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb774083bc57341f4d16e13523ef28ebaeb2ba5e458cb49e90334ff82096550`  
		Last Modified: Tue, 02 Jul 2024 09:49:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b734942366986b9caf0ce686d233280d4354389726838d88e05b383e1722f77`  
		Last Modified: Tue, 02 Jul 2024 09:49:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4353decab99c02db1da2abd5ba9b56e48e541fa8856192e82bf0bad5633f5077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dc6e0d0c0531a7bd085404b76a4d4cf5095f12beee962a33f339a2be59ad1d`

```dockerfile
```

-	Layers:
	-	`sha256:13306327c534f96cea0dfb29b8d1c7e970b2ed19c70d8f7e7f2cb145fc6ae8ec`  
		Last Modified: Tue, 02 Jul 2024 09:49:57 GMT  
		Size: 4.9 MB (4915622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d523308f225deef0b6840fcae7d33c707bab0e4cfbffb43ba9c99903dc756f0e`  
		Last Modified: Tue, 02 Jul 2024 09:49:57 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
