## `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:a0f4593a607d234a60bc1eb8448c47298fd1a569b5c4f93788d965ac66bee041
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d08e5a62ee64adc9847d3fc782e7d0fe72a592707a9bead440fb13a4ee9dd557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250055826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1756da15b4a16197750a25dff09c70fd86331f759478064c3fb10544f6146f11`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5268f7c407efdbbd4376fc25470a595d27371dbf8ce62bf9fe349b9163cc626d`  
		Last Modified: Mon, 09 Jun 2025 17:18:00 GMT  
		Size: 145.6 MB (145635655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da297afa980b0a0988b6bdf46d310ed08f1171b325535b555ceca84a2b7dfc6`  
		Last Modified: Mon, 09 Jun 2025 17:18:43 GMT  
		Size: 74.7 MB (74664141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cdd55e459931fbbe88ab1f772b3f4047c64c3b294ca4f9ea1922a9be59490a`  
		Last Modified: Mon, 09 Jun 2025 17:18:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3396e0c44ab532818c86870f77bb953ee516f608b7ff96cbfc0b1c15cb3e9767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37c3437470301e1baffbf10fbfa0f0b846bf76d192a687a55fa40b84ff4d710`

```dockerfile
```

-	Layers:
	-	`sha256:0942b7b2762e9b2ecd8c4b8428814c1d24be6cb2d8a9912c67221a56b20ea063`  
		Last Modified: Mon, 09 Jun 2025 18:36:21 GMT  
		Size: 5.3 MB (5272425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ce935069d4207cd34e896232e00c1160403fabba103fea09cfeb0dd2d9e0d6`  
		Last Modified: Mon, 09 Jun 2025 18:36:22 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ed6be9cb4e05a3d3fed4ed6b7a86c9dba0f2496e575bd819b46ad184bff0a9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247508086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c0956c9dbe5c13a739e412de2075cee4e8f56b3ff768e4c80186c5e6d178d3`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bffa601d4109bfae01c726b3c589fd4f5f2a729cf77bf75617f68d7e04065b`  
		Last Modified: Fri, 06 Jun 2025 13:07:25 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5806fb25fe87e04858c829fcf29971c564c73e1ea1360ed4a8f84aedea369786`  
		Last Modified: Mon, 09 Jun 2025 17:44:21 GMT  
		Size: 75.0 MB (74967323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7cfd735b5d257ccead5174a77853ee17f2cce6a926298400d78fe80d2c8c21`  
		Last Modified: Mon, 09 Jun 2025 17:44:19 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43ed0e7b77282c343967f794326a3a8e0dbc212a1f1aba06c0649f6999ced1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b11d669d3bfc789a2a35eeadf320f0c45ce8a935eea9d7598a543a91c7d48f`

```dockerfile
```

-	Layers:
	-	`sha256:17ac37e7e24d7db13c3e67fc3d5a4213fcabd0266fd47a859953805262cebd18`  
		Last Modified: Mon, 09 Jun 2025 18:36:28 GMT  
		Size: 5.3 MB (5278812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb092bfed3c6ef7927e7ed376ee4da5477d1522ebb14870137600430376b827`  
		Last Modified: Mon, 09 Jun 2025 18:36:28 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d9d1a6580448e8bedd371ccb1f5ea809db47494aca6cee756984f79432b78668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246793587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfd157e4c4fa313b7de30de2e996043646d2cedfd0964be731219149811a3b7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c18682abc822fc2db69cf01e2aaa0cd74ec88d2153d1db29a25210375b8100`  
		Last Modified: Tue, 03 Jun 2025 08:33:50 GMT  
		Size: 132.8 MB (132810533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28019e57430b168a4f8a782380d3fc81f9a8dd32afca46a45da96c4fcad9cea3`  
		Last Modified: Mon, 09 Jun 2025 17:59:11 GMT  
		Size: 80.4 MB (80401846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02924fd90e3e26384fafdb9429d972d81d52ada9a93168196480631c91a17b3`  
		Last Modified: Mon, 09 Jun 2025 17:58:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:101f9af9917ee77bda34dd5990f8fa0815ecc835afba76200942738ca9e51896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9041c46b63dd1312c7cd81614e0a7cfbad7e9c8b4f23dbfb436363149f88a458`

```dockerfile
```

-	Layers:
	-	`sha256:e57ea2f839ab3ad61490b487e72f76fbb77f351f273739cd212dcdf2a8afb5f8`  
		Last Modified: Mon, 09 Jun 2025 18:36:34 GMT  
		Size: 5.3 MB (5276181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3e74ae9d72a71cc0318e8bcc2a2eaf66f5f111c7a563d7377152c3adf98fd0`  
		Last Modified: Mon, 09 Jun 2025 18:36:34 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json
