## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:0ba4b160a64541bcac221b876c29f8a419a6f81defc1966ad5a56e0e572d5064
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:36da9582c08b04cb9c9da1dc08eb75085f48b3f2d46b1585b595aa1c4872af12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242391343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e61da381f65151890f0706fbb7bc6a019cbfc2dfe00c3562d2949ff5aeb821`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae348cac5dc9e7ea442c18f0f79f58dffb6108e8522802f50cababd4dbe6ff8`  
		Last Modified: Mon, 09 Jun 2025 18:42:58 GMT  
		Size: 144.6 MB (144635014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0523b8a4da242adba176e0529d3a5748f67829cd1b348d13cff41df13bf08fc9`  
		Last Modified: Mon, 09 Jun 2025 17:18:41 GMT  
		Size: 69.5 MB (69529958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702f29f28728e4d05fbc13bde072008abc685475921ca4637c8b098be0d0b8ff`  
		Last Modified: Mon, 09 Jun 2025 17:18:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5325d49786d875506eb1561b1cc2199a341c3293842cc6ada05fa301e84823`  
		Last Modified: Mon, 09 Jun 2025 17:18:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:374ce79db90cfe23041ac13c70370a307347cb1515bdf1e4a81455a0322a28f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f95cdb86f167dd277736980635b23e594cfc87b88e8840fd51f61433c1e2e0`

```dockerfile
```

-	Layers:
	-	`sha256:eb2982ac52a83adeec2672ac6101d29ae31fdd6384ce37b5bc4d64d847c4e105`  
		Last Modified: Mon, 09 Jun 2025 18:37:05 GMT  
		Size: 5.1 MB (5109888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb25162ce2b6c32e44ba2c8ccdde8702e5878b88477408f506167bfdaa544a6`  
		Last Modified: Mon, 09 Jun 2025 18:37:06 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73238a4020267bd5a124bc23a6674bcd28d244da255de956bd76363170ac49ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240969862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbfc666444950dce34ea2962f98cac50b2ad20d3a8296ed096962a700c0dbef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbfa317a80df2e7dc3da8da387d9081ffa13f5e29daff53d5dcef29b40af4a3`  
		Last Modified: Fri, 06 Jun 2025 12:58:43 GMT  
		Size: 143.5 MB (143512643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb07ac58d559352aab2393d75f64160fb901df7d1d9f41788154ceb1e08dd9ca`  
		Last Modified: Mon, 09 Jun 2025 19:41:35 GMT  
		Size: 69.4 MB (69390900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349c88462ecf7fca77fe65d970114fa32400fa032775809b2f91b46c99377c85`  
		Last Modified: Mon, 09 Jun 2025 17:47:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de25f898d6d1db9b7b33fe1fb484367904e3ce0d05bf794dfbc47e13b5d6133a`  
		Last Modified: Mon, 09 Jun 2025 17:47:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2e97abf51c84faad36cbd3c059fd161e58ce277057fb6e572fe5d7de61ede24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debbb0aeb816e2001700a8bebb9eca36cdcd1f799a5d1505d07350ce2a7908d0`

```dockerfile
```

-	Layers:
	-	`sha256:c240302711dba2a35ee40115c1595bd8ee4e2da695dbb6ebc59d7cdd9f1cd234`  
		Last Modified: Mon, 09 Jun 2025 18:37:12 GMT  
		Size: 5.1 MB (5115649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f317b8ad95b38b6009048a042b9c11c9c105f0d40a4edf4a5cbfd67b53459d8`  
		Last Modified: Mon, 09 Jun 2025 18:37:13 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f5e52bbd0e8755daf8f636b81adebb3cf3bd32bc3309a00ae15cb6e715efb119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251694121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9addecf5b3f1b6ddaf6fcadf46ff1050da600c28c1056bb3b6f9f979f0595f05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07686e6fdd26baa61178aa1b8e90f5239ab4c91006e539b5fbf39feb82e0a434`  
		Last Modified: Mon, 09 Jun 2025 19:42:06 GMT  
		Size: 144.3 MB (144280562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6131ce70b0351c2a1dfe2fe724d6cda5f14eb7694598197c1bc91488b576f67a`  
		Last Modified: Mon, 09 Jun 2025 18:02:46 GMT  
		Size: 75.3 MB (75345603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcec4c2898f3667aa1d3c219caa0b81276d4a44b962a85248f61677297ebf72`  
		Last Modified: Mon, 09 Jun 2025 18:02:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972babe25153a0d1f20276120870fcff92ae1406df8d46abb3df11ea3492a6ba`  
		Last Modified: Mon, 09 Jun 2025 18:02:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9fa9b222a8240cae4747a338f0ae34539a39a3107d82b0efce860b3962125084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74ebbc87216f0b19084d624a57cf5441691a47ec88c8d49a4c6eb67540019f`

```dockerfile
```

-	Layers:
	-	`sha256:963719cacef53dc8bc0561686aee4841d4a51c1c6ef86677ff27cc003b2f3c67`  
		Last Modified: Mon, 09 Jun 2025 18:37:18 GMT  
		Size: 5.1 MB (5115046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667411f88ec68ce63a556ebcc5a68d0ec282f33582ad5d09e45a479c3d3cacaf`  
		Last Modified: Mon, 09 Jun 2025 18:37:19 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3de7906b905c83fb8d75157fead89f785663ce579249ae5663e1b052a8373c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229891397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5225dd0f3b75d969c0368544077f739f37af1b58ca2228d21bb6d5c13661106b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad34fa5b937772a939247553d5da11fa707ffc251f370c152ab8bf4d478cc3f`  
		Last Modified: Tue, 10 Jun 2025 11:57:22 GMT  
		Size: 134.7 MB (134673554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e089d9e4861d81fb88c09e6b64ab9b7a7a544c0470c8cebab661ac95d6e86522`  
		Last Modified: Mon, 09 Jun 2025 18:47:17 GMT  
		Size: 68.3 MB (68333990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363df93173faf3d354909007b547cca9cb81dcf1a3be06705e60de227ff32a88`  
		Last Modified: Mon, 09 Jun 2025 18:47:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc89e3a4c58069edb1b92f0ed18f166fa0000c1127885349fb29334c7b0dcdcf`  
		Last Modified: Mon, 09 Jun 2025 18:47:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06dfa87baabd9d5197d7f6dc2ab17cead5c745021e9e3416fc06cfcdf3b765f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a1b0fb3948639a5ee72c4ae386d0aed7ee3bdc92e0f78c4f29a4fc8edc33ff`

```dockerfile
```

-	Layers:
	-	`sha256:89891de19314b5096fbaa42908e31aa8a906f677cf9d8788ba9506ef4779b63a`  
		Last Modified: Mon, 09 Jun 2025 21:35:59 GMT  
		Size: 5.1 MB (5101209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b11ca3b0ee68d7ba76167e61bf1b3e4726656e3d0e7487bb2c6238abfb5627`  
		Last Modified: Mon, 09 Jun 2025 21:36:00 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
