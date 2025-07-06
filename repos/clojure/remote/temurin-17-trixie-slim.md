## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:4a307b6f83cfe17c3be53722f7d7cf2e313701bad7b5818a4cfd3d00af84e8cf
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dcfefe382046f15e76b701fb93647a816e61aed2d098779136f9a370f19caae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246209014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6318913c014bef4d005762261fe247645e62c776f9cc7d9cad04b4f7565daaf5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eae6d19ba162079402bcc9a2237cc5b6f146bdbb178adda2de7923ba14b11f`  
		Last Modified: Sun, 06 Jul 2025 03:30:32 GMT  
		Size: 144.6 MB (144635030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ad9257fa223cad4847ac2fa2bbf7617e3d5b6303702f187cf6644bf0a938b2`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 71.8 MB (71811838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba473110234f6fcdf3b44ec4a10c97ad370606a0de6925cf602cedd74e0b990`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b28f6974050760016fe95b4dab7f03d3c5988ed98eb08d4098a927033e25151`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34c73892eb5576f740e143b8f34c4e2cb32960c02957c6fe2c343c9550a06248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f020dbc221febc18e96815b2690279391c0a7b225b4ff08bb62917481b4b120`

```dockerfile
```

-	Layers:
	-	`sha256:20cbaed44089b33d460f04be89f9244c82a25a5545e62862a4f9dd0c03a9af8a`  
		Last Modified: Wed, 02 Jul 2025 06:38:54 GMT  
		Size: 5.3 MB (5252802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3458bef1216d0ef18e03858d5141afc8ba443298bf109061e8adc65b47a1d3`  
		Last Modified: Wed, 02 Jul 2025 06:38:55 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd83710dd5386857a16a42f532334a872d589876ad1f30dd77a26545f42d5d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245282841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc48c5719f5bfba5addb915ee945a428a340cf184cd83e901a7a8ce6d3251565`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704b9114b691c79a543f54c1c754afb7a397ecb25d8ca35615f1edbcafd40620`  
		Last Modified: Wed, 02 Jul 2025 16:29:36 GMT  
		Size: 143.5 MB (143512636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aac94ca029d14a94924b62b97660ae1938ae78a2275e02bb064bc5c7cbdfe5`  
		Last Modified: Wed, 02 Jul 2025 12:41:18 GMT  
		Size: 71.6 MB (71642297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a814c2b8d3175d336d645456b62670f94b7c06ff56ca81ad1ce56f7d413272`  
		Last Modified: Wed, 02 Jul 2025 12:41:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9bdba8db677e4e079db63a2c09dc5817e1deb4d78699cfd2d411e448447f53`  
		Last Modified: Wed, 02 Jul 2025 12:41:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:387fcf3faacf3b234a1181169da120d54e42142913759695f71fec8fe9541659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681e96db287b1da36c6cfab35b0aeef2dcc99fd4f3eb3b6ab6772fd10757d1e`

```dockerfile
```

-	Layers:
	-	`sha256:76cd7afa6285c9b13079c39a214c4a6cfdc45e1379d01efbaed0638d80f3beb3`  
		Last Modified: Wed, 02 Jul 2025 15:39:07 GMT  
		Size: 5.3 MB (5258571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319714a5131a2d774a22ffd424475c2e5a2d5714cbd3326461e846bd333d5109`  
		Last Modified: Wed, 02 Jul 2025 15:39:07 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:427ac8a18464ef52972eba1600fee89270d078150456ed5a42d9b01fb59660e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255100370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7632d27431103798dcf8758efe87e9161bca95ac27d58c13011558c846022596`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3a30112808e463af488dbb6e114a2eec83b9cbb9b6f3f28ff509af0a0910dc`  
		Last Modified: Wed, 02 Jul 2025 10:34:37 GMT  
		Size: 144.3 MB (144280301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1198213981323bd8d8de898e3ff4b3601881d431d113f3544e162f36ae45dc`  
		Last Modified: Wed, 02 Jul 2025 10:43:15 GMT  
		Size: 77.2 MB (77232992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0dc099e7e81f159c8724ca38f1e4ced7ac6f703dbd15e003ccb3ec8f349a64`  
		Last Modified: Wed, 02 Jul 2025 10:43:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8260961c8ac92c6317b7e0a2a3a9ed5d04591b47a7e1764fa6e2e74bdd13068`  
		Last Modified: Wed, 02 Jul 2025 10:43:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12a0610732c3743bfa8f044518b9cfaa339422e72cee370ff195fc9d564a3a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839804da961d23e495a266560607d3b16f4f2ef6f01852bda5c98b0f1c7dea92`

```dockerfile
```

-	Layers:
	-	`sha256:5d051ad8f12310b30bbaca628a5f30b34ff0868ecb2b588ef122eaab33a5ec4f`  
		Last Modified: Wed, 02 Jul 2025 12:38:29 GMT  
		Size: 5.3 MB (5257173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e428f62357f13b10ca8a289783d708752dfc1170b3c468ad9f97e058487c138`  
		Last Modified: Wed, 02 Jul 2025 12:38:29 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:f547a61f03ccb5832726993751725bc6d9158c9f69984d13c7d9354dc4b64366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237455500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e32d1395292d69430ca64fc5505aba2a80897b0ebb3beac8497ecbf5a941ab7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2b65233e8143be1a95f017724bb47e4aee50f74172d5cf6530d4fab016a32f`  
		Last Modified: Wed, 02 Jul 2025 08:35:12 GMT  
		Size: 138.5 MB (138492472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaad79f9d1bd12de211e86f93bd0f2a766c67ce4837b3438374370f22d702e43`  
		Last Modified: Wed, 02 Jul 2025 08:55:45 GMT  
		Size: 70.7 MB (70703020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f309b266a17896bc017b2e2027e43e67fea91163a53dc8f4c6f6699eb4a3548`  
		Last Modified: Wed, 02 Jul 2025 08:55:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f7191c8cd10610f7ea03968eb5d3eb1d734e3eba8348a81838ab1829142fc2`  
		Last Modified: Wed, 02 Jul 2025 08:55:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:63a9b947831e4db14510995cae793f1496cc230e3ea5fe667e0fb28cab015e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5256250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82b27fb96b4351831cfb6ba1d285410a39c7946c175c9676fd31e4d9a3bb199`

```dockerfile
```

-	Layers:
	-	`sha256:8e9ecd69e0cb3dde7ab878c0b6d043fcedf1417b34f25a30adb8a4c6d95a84b7`  
		Last Modified: Wed, 02 Jul 2025 09:38:32 GMT  
		Size: 5.2 MB (5240347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39dbc7b6c489b8ef60828365d004562bda528f52523ae55dda79988a93e10dc6`  
		Last Modified: Wed, 02 Jul 2025 09:38:32 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3e24280cad814fb37a18c157551f41b21ce901b623cc256b78444016ff9b2cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237315245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c92ec796fca1d2b822c927b0ef6c27a0bdb15d070b04908d56fd9db22357ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a718f309e1daa9dc1ffe6f33a1e3e1178c42601fda78f78fee1be24453255a`  
		Last Modified: Wed, 02 Jul 2025 13:43:46 GMT  
		Size: 134.7 MB (134673590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954b20e9710cc9496132cca226fa268f5ecb64c87eb4c57e24bb0bf9c18f2b1`  
		Last Modified: Wed, 02 Jul 2025 06:44:20 GMT  
		Size: 72.8 MB (72802271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741c1604f533e7d30057c5ee41c59d83d0b41ce8505dbe22c35cfd5e75dc61b`  
		Last Modified: Wed, 02 Jul 2025 06:44:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438117f01cba53c240f9d9bbbf5ccdeb7f90b5b66c6441ba5d78e7270735c96a`  
		Last Modified: Wed, 02 Jul 2025 06:44:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd35869b61ef61ee28d9ca0f713bab0e3d6ce67987ec3fc952783a8697ad7aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bc5ddaa6baf646dcea2c6b7c9ffc62ac5733360b7c4789430fa077992cb6a9`

```dockerfile
```

-	Layers:
	-	`sha256:f53f54aa59d621e6ef0365bbe3dfbdaabcddc3e7598c627441fb4dad823c67be`  
		Last Modified: Wed, 02 Jul 2025 09:38:37 GMT  
		Size: 5.2 MB (5248726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44628f7e00385a97fa57a0e4cfe3ca0ac9308fa9443c3214f5156de9f863e787`  
		Last Modified: Wed, 02 Jul 2025 09:38:38 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
