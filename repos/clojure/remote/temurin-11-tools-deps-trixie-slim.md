## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:6bb75b8c59097f13b690e605de5da389999214f00954e33cef276fd2665a5ca3
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c2856edb4d1e2e3cc6ea89521d206224185d86092684463d4bf8620dd1084625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246740094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c222e07f960d8e2d4949df907bd5941c12f46d77b74c1b343f3b80bcf33db0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:07 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278f38c6d7ab51f6f05c991fe7ec7728f73be9adc2aa890e343cb24ce54f78f7`  
		Last Modified: Sat, 08 Nov 2025 18:42:45 GMT  
		Size: 145.0 MB (144966518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d403a296349e653575eac6a062993b1a99bf5114f6c68eb65a34bff0427107fe`  
		Last Modified: Sat, 08 Nov 2025 18:43:12 GMT  
		Size: 72.0 MB (71994826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f2bcb86b6b6dfe7ec0aed221c6da9e53f0ed6bdb26c70a754873458803f7b2`  
		Last Modified: Sat, 08 Nov 2025 18:43:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29b52deedf1d0af1d996cb119ce7314df64c5c5584797411846bac0b6b48928f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c66fae3c4bd4bc6b9205a5b79c00530c0260de8636fc77371cca9d807abcbc7`

```dockerfile
```

-	Layers:
	-	`sha256:06ade2c05c609d8168cf019fd9a1c9b272a52daf5b90a7fdbc2a0e9274831605`  
		Last Modified: Sat, 08 Nov 2025 22:40:10 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3846480bbb45f9cca55fd487be7a61bc70215934f0cf48196cfc4538d25e9007`  
		Last Modified: Sat, 08 Nov 2025 22:40:11 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70674b44809a7b84ac68d1718b56903ce523d2a43571278e695011cc35436dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243683087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f8d0270d417012422626b3d0d575d52c04a8067899176a8e18a2eb736061ad`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:41:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:29 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:29 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90057a63803b159ac670d744b0e7bed15a637d9adffc9b2bf8c39b05b378fc`  
		Last Modified: Sat, 08 Nov 2025 18:42:11 GMT  
		Size: 141.7 MB (141731668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948e71568c32748c1ce594e85593266d81dd8995558fdb976f9b2b1f0c8cc32a`  
		Last Modified: Sat, 08 Nov 2025 18:42:43 GMT  
		Size: 71.8 MB (71808477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc644dfd3224ce7b95ffcca76b63355c521e11d7702f4e61165fb1c6af6944ec`  
		Last Modified: Sat, 08 Nov 2025 18:42:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d4576a06c8aa7bd97231f55daf8ebf845127feb7f5290f62359c66d8bd5268f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcd9c39c4e6a3dc4da913fff7d4754a1c05b325fce6d644ee5b21ab1591c772`

```dockerfile
```

-	Layers:
	-	`sha256:c40d8e00d8a037670b9a7ebde470d00b8eca0da7c149fa6ca2f86301d81cd427`  
		Last Modified: Sat, 08 Nov 2025 22:40:16 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70580fc0f037421fdfdf285d28b4825ed8c976d1547522c8fc7c40adf2dd4d80`  
		Last Modified: Sat, 08 Nov 2025 22:40:16 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d5dc58acaeba7a936e8dc3776b4ab0c88fafb37542b5099896ac38257f32ecd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243075956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313f26a27d4c542e85c31e52a9c05ae37cc1aa7be4360264900328fb18299350`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:29:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:29:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:29:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:29:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:29:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:38:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:38:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:38:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e84755afedfc1f89c7dd573185b292e927a21b944ec113aeea516c2bc3165e1`  
		Last Modified: Sat, 08 Nov 2025 19:31:00 GMT  
		Size: 132.1 MB (132079869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a55ce9b574964f78dc82c5bec18de97818c78755b6e3062b34dc93ffce9571`  
		Last Modified: Sat, 08 Nov 2025 19:39:08 GMT  
		Size: 77.4 MB (77396793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620f9b2cfb231ec7f0e46b335b2a1de5344d1dd52c1f4b02b3b2f0e1f4ad777a`  
		Last Modified: Sat, 08 Nov 2025 19:38:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d2bae97aac719f8fde5b0b8ad63f4f5458c9aa05915f93b6efc730ef69fc1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b894c5530c8332a5bb02b9531cb4601568cd083f9928511dd1fb0ffe633d3aaf`

```dockerfile
```

-	Layers:
	-	`sha256:30087aed0beb75f1d62db0e71db4f888e2599b0d6719309e680e2e6cc23113ca`  
		Last Modified: Sat, 08 Nov 2025 22:40:21 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e9932a99f9f945f6d0c545c50bc81bdc0eb8d7ce4655528d7dee08328b115f`  
		Last Modified: Sat, 08 Nov 2025 22:40:22 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4a7cd33f5e91c26a33d2f7e5ace6e2a69a3648df9fe9f657ad8cf7f9cb3a9003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6021bff3b7d254eae775a80edf82aa6250337b30305b727705f3e7eccea9094f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:28:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:28:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:28:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:28:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:28:48 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:35:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:35:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:35:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f099d59af03fe6bc10258e94c860b2994d275fa9662ea68f766b2f81cf78fc48`  
		Last Modified: Sat, 08 Nov 2025 19:29:55 GMT  
		Size: 125.7 MB (125694374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d28cdd2e2c867aad3f75afbf855e8e51632cb66c3140c5ae4d1c995167b77c`  
		Last Modified: Sat, 08 Nov 2025 19:35:46 GMT  
		Size: 73.0 MB (72953594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f217504d4c137cf4af86b87438cd918efaf24edf5d33458ddfbde7f1c6283`  
		Last Modified: Sat, 08 Nov 2025 19:35:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f13bdbfd1a51ee12e0a5f8c724b95f6dc86dcd23de87e27f46e4a82996238502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91710db09c1c43e9f77c9cf6ff4628880e221edbf20c642ef1deeefb8b7f015b`

```dockerfile
```

-	Layers:
	-	`sha256:9bdf4902dad1a843afe2fc6d6de8436e50a14262cdf26793d6f27a658a442e90`  
		Last Modified: Sat, 08 Nov 2025 22:40:26 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0754ffe16e6843484a1e35f33046352bafd83f389956c71c1e1484069cf56d`  
		Last Modified: Sat, 08 Nov 2025 22:40:27 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
