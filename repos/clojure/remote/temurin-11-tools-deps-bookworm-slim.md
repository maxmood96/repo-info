## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:289aaefdf21c828051d5389d314f5325725b9773b7edfabd370308093c8dc08e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8dee0489b2a3c24308cebfd21928f59ab59b690adc600f181758ef8769af4af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243341117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7f5f01487f58a1beacd9f7ac87058763a244229f1e8a4b87d205df2c5993a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905b1c3da988c994ef048fdfd571442bb0b1e16dfe9656f29ac0cdb3a9aa70e1`  
		Last Modified: Wed, 22 Jan 2025 19:42:21 GMT  
		Size: 145.6 MB (145601449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be5288df7a2b0eadf53218138b06b31dd8b80c02d005d1dcb7ae2da2b3de676`  
		Last Modified: Wed, 22 Jan 2025 19:42:25 GMT  
		Size: 69.5 MB (69526607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c27714c032aedbe087d816ccce94ccc1d0688432e91a4db687cbff08de0b4e8`  
		Last Modified: Wed, 22 Jan 2025 19:42:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2af3721e6bbb54856615e0c481555ca651129903d0fb00b056656d5a598a8787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f296c832f4489f7d4cf2afa1bf068956a4a0403fc69fb03551997d1503dbf426`

```dockerfile
```

-	Layers:
	-	`sha256:c190653ac373abcf1ce7dee0d4a1064743e547c357bfa380827a2f09a180c7ae`  
		Last Modified: Wed, 22 Jan 2025 19:42:19 GMT  
		Size: 4.9 MB (4932708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0478d80567038fea1e57d40568f64f7b660df08d57c0d86a384f4ba568205000`  
		Last Modified: Wed, 22 Jan 2025 19:42:19 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:645b5bf0b5fa06b018ac0894fc2b402ded6fa5345e35598e0d381c1680f52c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239804926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387eb2ee11a56890d1733977a4cc6496e9aee8a8069ae741eaf09cc39d3841ce`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9b325a9c371acdbba4dc04e0f86092a0e34b1287eb3474c3b83c7f10d8681b`  
		Last Modified: Tue, 14 Jan 2025 12:21:16 GMT  
		Size: 142.4 MB (142389009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f3d4c849a86ade7f86a756820869cde28a45845391459bc5032efacaa809b7`  
		Last Modified: Tue, 14 Jan 2025 12:24:28 GMT  
		Size: 69.4 MB (69374242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d1f58fe76a0c81ed7fb921aebc515eb81859c0d4a5ac38a01ff880a89f7e51`  
		Last Modified: Tue, 14 Jan 2025 12:24:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4cf24cbc09d5beadd831c83748c81add2a197f92bda39c13a6b45f568293070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb3870a582e1af7576d22d1ab83baa42f8f8689e23ca7f314f4d1d42c86397d`

```dockerfile
```

-	Layers:
	-	`sha256:2c9d3b9656d2402e615d3f9923ecbc0c00bbaeceed5c20668338ebc9c7c26f4b`  
		Last Modified: Tue, 14 Jan 2025 12:24:26 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d598831f050740c21e5194599f0ca082e65d1597c9250804fb35e3ee5ddb4c`  
		Last Modified: Tue, 14 Jan 2025 12:24:26 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
