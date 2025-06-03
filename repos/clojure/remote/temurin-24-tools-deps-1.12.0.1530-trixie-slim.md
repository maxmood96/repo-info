## `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:93c249bdff2687d4dac4986495bf4c9e4b4fe5b9cf5c207bf45dfa6bf02f6b1c
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

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:719ba2cbf09d78485564c18ba210162dee6ad7b6e1f765a40860964d80e7f4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194382809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c1dca7b2eb45f536f862dbfc889974637160e893d1e8b8a1ead3167f99eaee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc86bd58cd0afaa65d917ef01e60beaa668dd73a51c501ee92ab52aae941769`  
		Last Modified: Tue, 03 Jun 2025 05:17:13 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4e614a08bce0ccf209f6b802d316829a68ef1c115de0f7e5d4068f03af2f55`  
		Last Modified: Tue, 03 Jun 2025 05:17:13 GMT  
		Size: 74.7 MB (74674366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a213fb040817b464b4810351f43205792bf486549d65f792c3aa7fd67bfcfd0e`  
		Last Modified: Tue, 03 Jun 2025 05:17:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822c26f1852b6a41fe6e00141cfe5bfc897dadf0fe1beb0ea33c93a27028d8e`  
		Last Modified: Tue, 03 Jun 2025 05:17:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b775dfd45db603b1447af67085f062256ce3b94cb22f94bd8dc9e655000def16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729edae7edc5d4106c312a789dc0efe0cd5ed253b81bc888f75885fb7298dfc7`

```dockerfile
```

-	Layers:
	-	`sha256:7b5df4fadc2b67810b8adc2dd8882eec4c1fc35ebd2837283467131a357cf3dc`  
		Last Modified: Tue, 03 Jun 2025 05:17:11 GMT  
		Size: 5.1 MB (5062711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb0361fd519cb55397c98133151f3bdedf06d8422bd9a4f0e499599790315e4`  
		Last Modified: Tue, 03 Jun 2025 05:17:10 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26d78313a41d0875ea77bb18bee7360afad79e4297c1f516c52b01e47ee0081b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194170560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b419101394d45048732ba963ffff893f438e686d6f2b5fd84612bcc4eb45f099`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9eae18b910302d512424dc442cd7d56bf789911ad2568ced024da733788c71`  
		Last Modified: Tue, 03 Jun 2025 11:10:25 GMT  
		Size: 89.1 MB (89091283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bc1b07c02e84ad92c1850f13d2309c36cd3d672be7e0a37f6722a1ce4edc26`  
		Last Modified: Tue, 03 Jun 2025 11:17:12 GMT  
		Size: 75.0 MB (74958781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5ae2c35e904b1061cec98eeb9941556128df17f3e15b57ab762b841914a5df`  
		Last Modified: Tue, 03 Jun 2025 11:17:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e842c11c689251b5f1a7567424160ee7ca059b2e28e632ffaa11ae38d0ce7176`  
		Last Modified: Tue, 03 Jun 2025 11:17:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:67900c3a567f1310a2f4201915568217422315d948e78f003caa60eacd716151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3736f54bbaf745e18a4fe92924c6b89eff45250cc5ba8268b78660e84b24fab7`

```dockerfile
```

-	Layers:
	-	`sha256:6d1782ccc70c78ef944aa96767477a0f5ccc3e31d7e3be7a8e23ad9da1e7929a`  
		Last Modified: Tue, 03 Jun 2025 11:17:11 GMT  
		Size: 5.1 MB (5068477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182b1477123b985812fcc05f39467ba9cac6d34f23a7635a54e1260fcb165325`  
		Last Modified: Tue, 03 Jun 2025 11:17:10 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:87e27e98a459247b8219451f680e6b4112d0729ab0b974e64f035a9d79d3b388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203916105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bf26c0af9f7235631447cdf88342f0f675e658c5d6e80521542df15eb5da17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9425324caed17cbe9579689cf7955835ba7b30d6602498824e5018dfaa80960`  
		Last Modified: Tue, 03 Jun 2025 09:32:38 GMT  
		Size: 89.9 MB (89920262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d836b2e6dc2cbb0debbd922ff853203014c6e1e07c044d491f94c42931a667`  
		Last Modified: Tue, 03 Jun 2025 09:41:41 GMT  
		Size: 80.4 MB (80414239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3da06e860e926963e6a656992207a18da576a61d006dca7d49e1263bd735e3`  
		Last Modified: Tue, 03 Jun 2025 09:41:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd26c764987cf2f3c3a7c123c0803f29d4b79c4e6010793a33a13d796b85091`  
		Last Modified: Tue, 03 Jun 2025 09:41:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1118300622a4f8f0cacffc20808e9b187365a259a1dc04ab130f7a3a8b7c0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7523296bbd3335c66ee7a50bd2e4b6627ca7fbb2e7d8f5647de21c1abe4624`

```dockerfile
```

-	Layers:
	-	`sha256:1ed88aa0ec045874b25683adbe927ec9ed25eea8e34a23891eddf7f53c2399e9`  
		Last Modified: Tue, 03 Jun 2025 09:41:39 GMT  
		Size: 5.1 MB (5068380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a269eb1c1e4f402cd0e225ec25b814bde3677ab874376bd6a2453db1d7ccde`  
		Last Modified: Tue, 03 Jun 2025 09:41:39 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:05ffdf624d9dd9d1917fb4e7c2fa7b15348d16b4083a08bdc0df5bcff86b4e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189159263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d27cd8892c634d8a2347869239d4c426a8494802d51ddef5e764f5900bf6b36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4940ebfc6f1c13fcbe1aced0ae631c0e454ff970d870d449e8b90708e20cd8c`  
		Last Modified: Tue, 03 Jun 2025 10:29:53 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a6f93adfdfaa76f76f7187bfb3cc627f2f333473a0674eda955ee7ce79fbe0`  
		Last Modified: Tue, 03 Jun 2025 10:51:20 GMT  
		Size: 73.3 MB (73290705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c9a97f81ad5a971cb6902374dc4cf54e6be8e9bf83e060352afca46ac9c2f1`  
		Last Modified: Tue, 03 Jun 2025 10:51:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb142732fd6dcecb350139c124259dad9dcacc2c5929bb75c6750824b2e0e1`  
		Last Modified: Tue, 03 Jun 2025 10:51:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e77e7667b2eb2cfced7beff1e9f8a9827048005614a02fdb9a23f9de4cbb0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f8dadd8814b10a01d43ec1832c4a4b42d2dcacfe41fb11b35b6d7be90015db`

```dockerfile
```

-	Layers:
	-	`sha256:c896d9125cd449b5c438d600d2fbf52996b9a5a93ecd5a4358c213167e3b33e0`  
		Last Modified: Tue, 03 Jun 2025 10:51:11 GMT  
		Size: 5.1 MB (5052172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a64e39e3aadfa3915e5142b7d331b0263389c8777cb3a8f97ecc2aba34f2b2`  
		Last Modified: Tue, 03 Jun 2025 10:51:10 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:32cdb93241e57c1e9321398bd191aa543f5d89ed5b34aaeed155b13c58c0aa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190453925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a192f51bf18302de2f01853e05f89bfadd2ebdbc850c37e5b66d80b54d625c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e16c52945849bd7ff81f8fad1acf7f6b275ebd424116d7c5e5b466881d6e648`  
		Last Modified: Tue, 03 Jun 2025 06:39:48 GMT  
		Size: 85.2 MB (85216842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7e1b80124566786dae067845209d75a219bcdeac7d57fe4edb6be863111a45`  
		Last Modified: Tue, 03 Jun 2025 06:44:47 GMT  
		Size: 75.4 MB (75406423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d88ede42b0a150be17b2e01115cc08bcbe5fbad93e0619f9266ca85539afea9`  
		Last Modified: Tue, 03 Jun 2025 06:44:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dc05aa7fc31f4ad7708a6424b7eb7923f14deee738195fae8cd25201b08011`  
		Last Modified: Tue, 03 Jun 2025 06:44:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0136c0329afd67be8d79c3222cd59533b3492c831f071f5cf98d7ef66a6b1ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2cd4f2780004a50c40f5a214da332fe84b82db66a4ef7f8dca76252e90fca3`

```dockerfile
```

-	Layers:
	-	`sha256:1da0819ea4b1b7fd1bd4602d1ebd8e218d6c4c72d6293d210f9dbd5ca95ec870`  
		Last Modified: Tue, 03 Jun 2025 06:44:46 GMT  
		Size: 5.1 MB (5061183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470367a2334e2adae7a6a16136226b0f1bf5674f2eb964f159e0103d02391df8`  
		Last Modified: Tue, 03 Jun 2025 06:44:45 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
