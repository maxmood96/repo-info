## `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:a2671fcef4d94e1463a30f22199b0f7c4aa92bd773b55ce96bfbce8adc071798
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:375e0f060c3a5ad83962c966cd9b8820d84eb6b830807c797817b85d13d00677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247114841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2370727223192f7589922974e0ac4714c147bb5696dafb1b60cf1f7031d751`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
	-	`sha256:6f052c0ff895d860a8f6983dcf5207c5e8ff5949529101bf68c1e92e9c8baf36`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 29.8 MB (29756816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07db6a10e5220eccef3462047aa19b906f5f72d06dffa1e46caf4bbccf4d08eb`  
		Last Modified: Wed, 11 Jun 2025 04:19:26 GMT  
		Size: 145.6 MB (145635641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa347ef4282d4000d0ca5aaafb83f5cfbcfbabded46b2867c6983e01b8fdb4`  
		Last Modified: Tue, 10 Jun 2025 23:51:49 GMT  
		Size: 71.7 MB (71721739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ead5cf29094e0cf1e36e5879e92235de649026991741f6a8f4f7ad02d281`  
		Last Modified: Tue, 10 Jun 2025 23:51:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d7a06dd4fb1f8e0ee1d0ec9a8f929dcace1b8c29081fceca5f17efdfcfbaca74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95738d70d4e949f5a09afb47ffd38be4115d4eb328013a926c287209e9776646`

```dockerfile
```

-	Layers:
	-	`sha256:9119b0e6d9d48821edca92f816ce85355dbe45ecfb02553edf6721424e1e1224`  
		Last Modified: Wed, 11 Jun 2025 03:36:19 GMT  
		Size: 5.3 MB (5272939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7e0098090954595911a5f260f058b1ed646f441bc961bb803c262614ff8a3c`  
		Last Modified: Wed, 11 Jun 2025 03:36:20 GMT  
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
		Last Modified: Mon, 09 Jun 2025 19:48:41 GMT  
		Size: 75.0 MB (74967323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7cfd735b5d257ccead5174a77853ee17f2cce6a926298400d78fe80d2c8c21`  
		Last Modified: Mon, 09 Jun 2025 19:48:34 GMT  
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
		Last Modified: Mon, 09 Jun 2025 19:49:14 GMT  
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ece9cb2ac5cf2f53b5118990fc5bb89238e7aaaf48c28648ca024d7defd84b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228238052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66608707d48e06f0e830ecfbf2771573143109a7a7948fb1c7735467cf497a3a`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
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
	-	`sha256:c274825e96bcfbbdcdc116bb72e2d5d06d51048380b2fb22f400e6f9627616b6`  
		Last Modified: Wed, 11 Jun 2025 00:37:39 GMT  
		Size: 29.8 MB (29831871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85716630e4cc2fa0e838c518090798d18c99e2cec7a331136cb18debf66e2df`  
		Last Modified: Wed, 11 Jun 2025 05:36:52 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8a73d25a59dd7dc0cd800214977c59de05d2c3fc278bd30178bb2fa2eff1c2`  
		Last Modified: Wed, 11 Jun 2025 05:40:26 GMT  
		Size: 72.8 MB (72820208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bfd27bc66217b79d57fd13d85114c518be0ffffc6c1d7ddbd558ba2f4a91d9`  
		Last Modified: Wed, 11 Jun 2025 05:40:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d9c5810d23f4b19dd1f7a08eb12cfdd81b812ffd9b3d85b81b89f3b39e8dba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2b09b8f1bb4fd3d0d7f525bd1f03654879a26713c1a50f27c69cdf93d3009b`

```dockerfile
```

-	Layers:
	-	`sha256:5a60f894205d8cbcf29e9c1195b0a2af8dfa323ad210998263a4e03de8214793`  
		Last Modified: Wed, 11 Jun 2025 06:36:03 GMT  
		Size: 5.3 MB (5268867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92deb80ee6c04d243819ae36c958f4fbcde8d4719ae2d8f03f6af4b27679ee37`  
		Last Modified: Wed, 11 Jun 2025 06:36:03 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
