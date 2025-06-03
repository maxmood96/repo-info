## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:ccc221547f7dc298dd8724716be8db3a610bff4bac5b8a78077e15b0cbd50a0a
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:82bb8cad39cd225d8b25105627ea33dcee0005dd54ad33019ef8f0faa80b3cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243392559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd760fa7bfe53ebe97f6cf46a5bec815a071f0b0790dfc746ef97ee6ad6e363`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c334ba08ed2fb69d58679a953992a7f4f9b91fb2d001c01ee51cdd6e80b4c`  
		Last Modified: Wed, 21 May 2025 23:32:26 GMT  
		Size: 145.6 MB (145635749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ac8d6dd45327dcd864edba5f930e3a9266ef55e805250492c5bc15908db5b`  
		Last Modified: Wed, 21 May 2025 23:32:25 GMT  
		Size: 69.5 MB (69530835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017204c092ecc9ee21ab7addce80b11919e0504626764726351bbacfb85c4a68`  
		Last Modified: Wed, 21 May 2025 23:32:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d387e32e5a729d5bc83a26991f98361092f5909bc5f800e81139505b7fe1bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4995949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adde3adbabfe8698a523bbc9e4578fc0528e0c866e94a2488f4dfe46007aee29`

```dockerfile
```

-	Layers:
	-	`sha256:90a2e575924470a330cba910907605a815ef2017cf24225b7330b000703b6365`  
		Last Modified: Wed, 21 May 2025 23:32:24 GMT  
		Size: 5.0 MB (4981639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5efb637beb714d29a40c6349023fbdc9c414e99cc88c1275084574b7d60ef4`  
		Last Modified: Wed, 21 May 2025 23:32:23 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a88cc3cd92789a987b1015429dd2f179369c42e34255feffdaf3377cd2c4011a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239872845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97032dc7096f711a87b8f568deceb5672ac4bc40ace1ba33a8abc96266ea3ce0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37350b9d182fff661b148558da9ed47009fbedca9d38d8cbe480308ffbe9b84a`  
		Last Modified: Thu, 22 May 2025 08:10:24 GMT  
		Size: 142.4 MB (142420719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766e65a46986942725e25a8a7fcd04a446ae993e92ec50a004d020914a5c161c`  
		Last Modified: Thu, 22 May 2025 08:15:18 GMT  
		Size: 69.4 MB (69386203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8478739e911f82c5885c32677756ba959b434d38e903a1dc7cf81692e2a9a6`  
		Last Modified: Thu, 22 May 2025 08:15:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:25e5be6e0bf010d9e3c225512e4325131660b35825737e3af458f8e6e17c4f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5002445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a4e4d71c2048e760d73693ac070747cd31b307af37cd13e0cdb7089db951f2`

```dockerfile
```

-	Layers:
	-	`sha256:528133687a6b54982f06d3dbac5ab32d8512577c51b40ce54006b9a9c2607a58`  
		Last Modified: Thu, 22 May 2025 08:15:16 GMT  
		Size: 5.0 MB (4988018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cda083903af58f89db7048ee495a33a7dd480acb407c00dc1a3bf4f1b30aac9`  
		Last Modified: Thu, 22 May 2025 08:15:16 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2935e09cbae8ee3fc906bee648904696e233b37c5a6870a1462e48813882102a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240224840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eea24c596c3be23f9a9f1c0901f5f25f7ef75328ad20055062ceb6a8ecb75af`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271db255539d134b82d3651d8652ad63172420be4a9a89df73d9360317307aab`  
		Last Modified: Thu, 22 May 2025 11:00:13 GMT  
		Size: 132.8 MB (132809834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f3d757780231ecee69325a9d0c4e0a72ccf3a613ff327a84df31baf8ce69cb`  
		Last Modified: Thu, 22 May 2025 11:08:44 GMT  
		Size: 75.3 MB (75347448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430f7d05712cafec7e1a500135f73e79b17bcf8f22b66b234501e460bd814aab`  
		Last Modified: Thu, 22 May 2025 11:08:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99e1c4de756f6affb4a4d786975b4e09c4bbea39395d936cba2ad3f801945b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f74aa5e04bc800df46cbb818d4da1a20b1f95e009fba7942a29825c5903aca`

```dockerfile
```

-	Layers:
	-	`sha256:12e2d5f5de8a1022b13e6201d17f5ab0f3feaf93450ac8aeb80455bc34710267`  
		Last Modified: Thu, 22 May 2025 11:08:42 GMT  
		Size: 5.0 MB (4986182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209a3e408789595ad65a3088511749756c84ae37a0878043a16eb72659a8159d`  
		Last Modified: Thu, 22 May 2025 11:08:41 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3fc39073d324666ff1a1500028a25172429d3373aa8c97eaad71e1676b5bebe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220796040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400212baedff5cac98c7853e2bfeda3d90f2079724350946ffac9f170007fbb8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed11ad230f06796b3ae1c13456129099ee497fa349ff5586d1c755ec5be7b03`  
		Last Modified: Tue, 03 Jun 2025 06:01:19 GMT  
		Size: 125.6 MB (125585354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c3386ab2ff9e61ec2f7500ee78d580935d2b22e775ddae68c0de1ef3d4e009`  
		Last Modified: Tue, 03 Jun 2025 06:07:10 GMT  
		Size: 68.3 MB (68327234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d929b14f37a205ccd25e2fe735b9d783ec4192fddd58fd8da774db5cacf51`  
		Last Modified: Tue, 03 Jun 2025 06:07:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b79d644e244f85ef25ff972fc440a0eb897add95e0a8e21bdb3122d1593684d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8320447d4e0800eb7aae8b72fa4e51615f6d8b9d90c60ca9646c006f924186d4`

```dockerfile
```

-	Layers:
	-	`sha256:4db509322db2609099ad60347bc23f261804a87582303513020dbfacec4f3b84`  
		Last Modified: Tue, 03 Jun 2025 06:07:09 GMT  
		Size: 5.0 MB (4975856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d0de48b60a512822aaeeccd7b51e807f7fd743aec2cb9d5f1076bd9714244b`  
		Last Modified: Tue, 03 Jun 2025 06:07:09 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
