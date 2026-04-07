## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:c8d43815ca87e115c28b90044c57a31b3fd0fc7f18d462a8b558a439ced512d7
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6e1832c8b3c8bd200ff712e986da40db71cb457459e81f2d6ad595a2c87487e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280672903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dea9bf3e9bcb49fd9752eb54305bfd59b429f6635c04dcfa7dcd73d53a5cc81`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:14:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:14:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:14:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:14:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:14:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:14:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad70884e684c89d0bccd605c3adec37e2e3741d0543537c18a7530e0ce635e`  
		Last Modified: Tue, 07 Apr 2026 03:15:01 GMT  
		Size: 145.8 MB (145806872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcb0f40ce80229f5ab08661d6b68f840d4ed0adc28cd8ec7e24719656ebde14`  
		Last Modified: Tue, 07 Apr 2026 03:14:59 GMT  
		Size: 85.6 MB (85567551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55d3bd68c40aa45a6ae365ca31dfa5e69effa759c17b6ba6ed3540290d4574`  
		Last Modified: Tue, 07 Apr 2026 03:14:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:82dc9ea8701681756baa45320968d940b392319e66b7f7015b06d933375851ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ef8df8522616ec8f110d75c36de67fc9d53d85735c0e259c1f2f8783dc2c99`

```dockerfile
```

-	Layers:
	-	`sha256:0025671ad14bf4bfdaddad22bb2b656243d18369c1cda18d377ccc78cb9c608f`  
		Last Modified: Tue, 07 Apr 2026 03:14:56 GMT  
		Size: 7.5 MB (7490808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54d9416f447817021dbb9968c1e136ce87ea6dc2a887b61d94a3be91853072f`  
		Last Modified: Tue, 07 Apr 2026 03:14:55 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7fadf012360a262c9ccd80729a1ace5aba00bcaa6f276e796e9f1ee854c888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277548908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a0914a4f54bbbb21e6c20183030f5fb5156c393259e3707187ee8af5560019`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:25:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb89399051b92d45beb86afca05500e7b3427471d1e6499c23f8bf1d0042b3ac`  
		Last Modified: Tue, 07 Apr 2026 03:25:40 GMT  
		Size: 142.5 MB (142500029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16bc5fa3e7deb66b54217f931f4ce11e0b8f0b306b7456a14ca1139d619d79`  
		Last Modified: Tue, 07 Apr 2026 03:25:39 GMT  
		Size: 85.4 MB (85382977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73af49cf236e722ad5053c31406ae443a5492bbe2379ffadfc553f29ec1c5006`  
		Last Modified: Tue, 07 Apr 2026 03:25:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a0c44b727c6bc5aac5c7325851ec8690745a65de47f0e5c763fc4e6172eb2f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c21306397c1f4c4e18bb09d8d80dc7abc3200e555aa65b8950661209a993bd7`

```dockerfile
```

-	Layers:
	-	`sha256:f74560a3c61c1d9f74a36da449738598f14cc0d579defc9b43f722bebc36d0e6`  
		Last Modified: Tue, 07 Apr 2026 03:25:36 GMT  
		Size: 7.5 MB (7498456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:864c39ff7a6be04a6601b3f9565c260d6c87288e17b59fcf2efeff91a961b36f`  
		Last Modified: Tue, 07 Apr 2026 03:25:36 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:dabbaa5a3c77ab75950d577b8d127e1a6c21f7c8206df7f32bb181396ec5d0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277102540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6904a4486ded7d00cd319557d73c970033b7055366a569bb081608647809150`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:18:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:18:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:23:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:23:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:23:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6d8bc187d9d77c2b576c45cef2edbe313dca76b0d35a49ca751f0587487fda`  
		Last Modified: Tue, 17 Mar 2026 18:19:41 GMT  
		Size: 133.0 MB (132996714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fcc6b71bc431fafc5c9a00de718a1dcc6211fb4b1bddad292a5d5d7ab5e2d1`  
		Last Modified: Tue, 17 Mar 2026 18:24:16 GMT  
		Size: 91.0 MB (90986830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22cb5c78e8eb8523c81e98568cb8db9d53bde873cf05e98be549140b90b5508`  
		Last Modified: Tue, 17 Mar 2026 18:24:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:377e8b4a06e1a6f12047cb170dc748d9b519bde16c3ea8435cf3e1929edd1fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c47c894e21152a9fbde8fc29dd5b022aa48b56d51bb59b7580e7e4e1849f29`

```dockerfile
```

-	Layers:
	-	`sha256:84c89bedf4afbbd442f19ba4cd916e39d0d932d8cfe81179765e5711b5bb94a2`  
		Last Modified: Tue, 17 Mar 2026 18:24:14 GMT  
		Size: 7.5 MB (7494614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ccb03a382bb8be95d055eb36ef8c5de4b903e10ebfdc9e56cbb46bb67f3e57`  
		Last Modified: Tue, 17 Mar 2026 18:24:13 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b90c4dfb5bd6f2860b1e255058cfff8ed38395a9ab4fae21b398f68debdd0f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262471881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8e0c5c44f389ccccd27dfd768e71e8ce19e1debece5d0b2e915c949e5d2b78`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:39:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:39:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:41:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:41:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:41:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0f6af54b41978b4b00c1cf75bd9972713058d469f37803b6fe31ba2949998`  
		Last Modified: Tue, 07 Apr 2026 05:40:42 GMT  
		Size: 126.6 MB (126562219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db28f8d40c7226ca446d17147551bf99e50f6e9b4241c3998ea991229c9abe`  
		Last Modified: Tue, 07 Apr 2026 05:41:46 GMT  
		Size: 86.5 MB (86543912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff24c24f3fa61f7817f087583f6d8d42dbfa29a10a443a3b504505efcd9f36c`  
		Last Modified: Tue, 07 Apr 2026 05:41:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9d253ff11cee3ada43deb75293bc1df6cdbfa1c017c67103ed1bacd503b90012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a29fcb64d82a8f35872937ec8c5b1ea15335aeb9fa96d6a7b27d3d763664ae`

```dockerfile
```

-	Layers:
	-	`sha256:50982e8c3e6a06e588c9db4d40e5c2c6db856f566907c3c8398c61a3020f0e7d`  
		Last Modified: Tue, 07 Apr 2026 05:41:44 GMT  
		Size: 7.5 MB (7486734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac5c63678365d86f8027b4e1ce3356a1182d8a6ffc2c442f94a07dbebfc2833c`  
		Last Modified: Tue, 07 Apr 2026 05:41:44 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
