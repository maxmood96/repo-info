## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:31b16c84a0491b3538b2880b65b788f397540bb6b4ef13380dbeafd2041fc292
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:88ef7c398477dd6a98c5fc5bc08d310c9f7cbce79131b927486e5648a75d5627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144138988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8a05a1311aa8209babd8008b933ec61919b80ad4bb486c7354f430c81e3fc8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798468f59a8358e8e1375320cbce3c4533f21e325c5ab5dd98712ad914b25a53`  
		Last Modified: Tue, 26 Aug 2025 17:27:12 GMT  
		Size: 54.7 MB (54731324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273cc022573d5f5febefae7438b49c2e393c78e4cf0bef75e00e59889ddb00cc`  
		Last Modified: Tue, 26 Aug 2025 17:27:12 GMT  
		Size: 59.2 MB (59150899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aca9072844d3843c542588825555f4b625ff87568d60faf1507bc3bcac560c`  
		Last Modified: Tue, 26 Aug 2025 17:27:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7cfd62f5057142ab015c71e547cef7cae027171a4ca464fd192025eafe8cb529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6ce717dfe2690dcc2ba4b14bf7bb5e72d1f07490831c2dadf33347876c30de`

```dockerfile
```

-	Layers:
	-	`sha256:752270d41a48ff438d6e7d295b236e2f84ef98018ef10ee243803268a78c8758`  
		Last Modified: Tue, 26 Aug 2025 18:44:38 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a629f1afdeb002509046df7b92f57edd7c0179c081fc8ef90733a4bab2932be`  
		Last Modified: Tue, 26 Aug 2025 18:44:39 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83096c2e4696daa2c36902f9e37c55138354bdae6bd0c964620fa45f97850bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141869646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e9788e80c64c54c51a629e3d353adf2288134df30bf0ebe7fc3e2c2ac69f00`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fcd2cf3916c34c7aa10452ba896bffac4cb7626ae6f5bb553f8058e5e491c1`  
		Last Modified: Mon, 18 Aug 2025 16:55:11 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e821268eaa67b3fc86b7e7b7eaf4428620487f54b68a49e2da5833f4890e1f64`  
		Last Modified: Tue, 26 Aug 2025 17:30:32 GMT  
		Size: 59.3 MB (59282902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68df93545cb958ad6d93c8d66d542a99891a4cf36665bd5bd0fb1cbd5c8fa`  
		Last Modified: Tue, 26 Aug 2025 17:30:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f75c3f94c5c36b7a48419b20af69c7f6dee241c40c44e64d544204bab20955d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb6f57bbc8c1ad13c7319d470fbd856738933ad759b37ac39d2adc6e1c5f722`

```dockerfile
```

-	Layers:
	-	`sha256:72af1d51d7bbb6505716f54fd82622f62fd008f0044595210ce6fa42d94e8646`  
		Last Modified: Tue, 26 Aug 2025 18:44:45 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a5e8de4009d95b7712dee0bf8d9fa9d25126eee3cec0b618d8c05825e9a7ec9`  
		Last Modified: Tue, 26 Aug 2025 18:44:45 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
