## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:de074cff7778572e3b8364e540d31d8b00cdb677b43a72e58718f430ef28411f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f52e3e1673e35902d31582c2eed1cd0247afb169c297e764a96477dd74d05a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190005915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6997173c294fbc5c3e35ad71dfcd827336e13017cb855e0e377b94cafac9ed`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:40:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:57 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b65b088f032e5191291efa6b35003bc2573f92c6b6c138da0c6d021bd2dc9a`  
		Last Modified: Tue, 17 Feb 2026 21:41:37 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3239806f8f08c5d6965ab959f4c423c69150786f01debb9f4a2f408c11b309`  
		Last Modified: Tue, 17 Feb 2026 21:41:43 GMT  
		Size: 85.5 MB (85542206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c136d0e0f7d09799ea367755c2dc5eca9bc56ce391513613271570456821015f`  
		Last Modified: Tue, 17 Feb 2026 21:41:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3e700e22a7b988b3b310ae4cf9223ece70c3f8451232ac07f2834f473deee52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6587cf0a033b150f094531cf5f5373d0c4513433c4e29fc7c8e901d91902e0d`

```dockerfile
```

-	Layers:
	-	`sha256:783be4c981a218800b06d4fc2dda90d0ff092a6a59284ac01bee010355cf8f5e`  
		Last Modified: Tue, 17 Feb 2026 21:41:35 GMT  
		Size: 7.6 MB (7590067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71eb6c3e912236ee28cc366f12cb9ce0a5df478b7b7edf0d8ad3ad17931b847a`  
		Last Modified: Tue, 17 Feb 2026 21:41:34 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cfad96a17a57a0c8bcc08f766ca2e0b75ff938d5c8ded72fec4ef8ce0ef929b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189266116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df1fdb1626ca80d13b17a986d498cced7e1ed27fc5744b592679be457af46d7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:51 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e0b2a24a45e2854487102df92152471ea582ac2819a228600161294b67f6a6`  
		Last Modified: Tue, 17 Feb 2026 21:41:33 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1619b0ea789762b91cab8b547f459a656457266ba8039b8291e2632230135235`  
		Last Modified: Tue, 17 Feb 2026 21:41:33 GMT  
		Size: 85.4 MB (85361841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4b34718b370bb68c5f59466afca966cb24ee7aa90818d8ecb7329a2f0c4870`  
		Last Modified: Tue, 17 Feb 2026 21:41:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fbf8f9203b874b5f826f8b65be40202cdbce770441e2d7e95862138ce1f62150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f465d6d66cba68cfe35f3fd98cb7bc5fb21f2ccbcd133a70df279826af51ec7d`

```dockerfile
```

-	Layers:
	-	`sha256:2c4cdaef6b41b8505f10b261539976a83587679bd24ea41056a8fed0c2bc8dee`  
		Last Modified: Tue, 17 Feb 2026 21:41:31 GMT  
		Size: 7.6 MB (7597797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39ed07544a7cb624b4824945787203a88598a56782650484ce511cc8a3f869a`  
		Last Modified: Tue, 17 Feb 2026 21:41:31 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:15f95d7f1b8f11e9be4d106229c1c67943270cb743be8b808f1399e61a751761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196710226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5eb21aee2d6a7cbe3797c43cb28bb6e983c8492616e403c085714c81586498`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:59:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:59:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:59:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:59:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:59:17 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:07:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e31da8e0f9e130c166e97ec3b0c716f0ac97a7e8894e13f7961b61b37819485`  
		Last Modified: Fri, 06 Feb 2026 00:01:40 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a4ba3aea40fc559907aed1c8987fe5d99a928d3b0eedfd7b978c4b55dc94e`  
		Last Modified: Fri, 06 Feb 2026 00:08:57 GMT  
		Size: 90.9 MB (90947071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b636d89a0392804a99da1d846f95ac4291d2ae62e0e7425076e2f9a568fbe76f`  
		Last Modified: Fri, 06 Feb 2026 00:08:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:48b92fc3953c8597fc9774bbff268f7ad9946bf3ce7f1c732a9fe41756634837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7609300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7ccb94ee8bf4435411bbde927fc2dd518b769f65d8151c3eadb66a1c934cbd`

```dockerfile
```

-	Layers:
	-	`sha256:8e2b4a04977b278ae156743c4e2605ec905e780540e1e6e923e7d380c408af34`  
		Last Modified: Fri, 06 Feb 2026 00:08:55 GMT  
		Size: 7.6 MB (7595083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e991ae055761181776fb38bfcb4b3cbce7017406d9098f0ea86d8b49adb661`  
		Last Modified: Fri, 06 Feb 2026 00:08:55 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
