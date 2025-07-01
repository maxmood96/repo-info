## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:e0f55bd85fbbba099b9fc436b1cae8311beb459e81f45fe706fecbfea91403cc
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:24b7a7f9cdbfea9503b190ed5723580f05c577e27593dc3a6f86ed40fe1cf362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247209283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef2c95e29826ca693248474310f79c724ac0ca728607b7822176d0e815a9806`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c007f3bcb7e5cdc56888ef71872415016cd5862f567475653636f3d34648965e`  
		Last Modified: Tue, 01 Jul 2025 02:39:18 GMT  
		Size: 145.6 MB (145635676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcb8c3470f62c0a66b8aa8c880c9942d04c35495fb5fac10693bb8bd2ff3a8b`  
		Last Modified: Tue, 01 Jul 2025 02:39:29 GMT  
		Size: 71.8 MB (71811856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afad3c8a09cf5f5a509ef21cde3a067f0fccc990dd446a1c719effe0833ae928`  
		Last Modified: Tue, 01 Jul 2025 02:39:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c016db049f5481e5a377af5d2e8af8c2b78780313941398912cc2cb984a60026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a5f8a0e837b5dea9a0b2abaed9d3067e3b7bc8167f8006a13d502393a97d57`

```dockerfile
```

-	Layers:
	-	`sha256:eb62b45e3d4081ccd3058bca41fbfdccb338c30af3ca5f77795315d14eb0a6fa`  
		Last Modified: Tue, 01 Jul 2025 06:36:35 GMT  
		Size: 5.3 MB (5272943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee067d59c18b3354459adc7bd4c966289bd204884b32a0189bd8cbc18441e77`  
		Last Modified: Tue, 01 Jul 2025 06:36:36 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c4f0d0b568aa606893a31e988490ba118e4b7dbb047a8b490c5440096f14c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244209737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134d3c1b8701899eda60e2b8e78e8362193e7dfe63ce7c4fc3088ea376302a9f`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
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
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e53b293f1fdac6d661d1a380287310ad1f0a58ef8bf62fd8224dd5ab24535`  
		Last Modified: Sat, 14 Jun 2025 09:09:12 GMT  
		Size: 142.4 MB (142420681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fedf014d80e648524333cd883f01d3f4e9ad6687cda3b4edcdac5a68f87c1b7`  
		Last Modified: Sat, 14 Jun 2025 09:09:07 GMT  
		Size: 71.7 MB (71667371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b969d02f8184d51e82bda01459de0726c4c8f3ee2328224b3f5610994edea`  
		Last Modified: Fri, 13 Jun 2025 00:49:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:611ef4c405cdbe8fddb93a0fccd07b4993d158ee478c46e95e4910f669241822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f827bf432d8142c233c81eed50096e6055313248d022bd06fccd26897970d3c`

```dockerfile
```

-	Layers:
	-	`sha256:4d3f5cfe802d3317531b018e342a9a7831d063c70431e5ac2aefb18d102eeafc`  
		Last Modified: Wed, 11 Jun 2025 09:36:55 GMT  
		Size: 5.3 MB (5279326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d1205ae2cbe684c570ffb4149cc19db5b58b5735a8411bebe7a03d50987cc1`  
		Last Modified: Wed, 11 Jun 2025 09:36:56 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:935da06452c5eba7265bd405322209ea7d9b0fede7be3f22b7cc4a013b2161d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243630092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99959491e12d98d2920cc5e8c114c84cfb22d67a143169b1570efa6b99ffefc`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed42b7a45be9a319908284c305fbff7f8a11100527571431a46ab61609503d1`  
		Last Modified: Tue, 01 Jul 2025 08:34:13 GMT  
		Size: 132.8 MB (132810556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae36720d6e361aa78efc5846c47c84a0a41df2716bfbddf9ad18e2401764b62`  
		Last Modified: Tue, 01 Jul 2025 08:40:23 GMT  
		Size: 77.2 MB (77232856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b100f07698ef647ecb64cb32356513f9d27f5f5e80095d6828f344f6a3076496`  
		Last Modified: Tue, 01 Jul 2025 08:40:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06242b7b8b10ec5c60f4224df27dc2dc655f05c4a9f1eb948a0d4abd41b2ff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bf4efca753514d3d7d6df6e1c8d87af79fce324b59bce988b9fc4ce04086dd`

```dockerfile
```

-	Layers:
	-	`sha256:fdd8e0389f8e8b331db5826fe41e4662feac558a2fa13207d75d2d1087c3f98d`  
		Last Modified: Tue, 01 Jul 2025 09:36:52 GMT  
		Size: 5.3 MB (5276699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37076908d53bb86eeb32e4750ab6ff1ace825c63286559e10e8cea4936fafe1c`  
		Last Modified: Tue, 01 Jul 2025 09:36:53 GMT  
		Size: 14.3 KB (14333 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ff749b610d799573be20cd1b1c3acacebb100c624de8347456437d84926210de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228226706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504d5ec15f9a13efe2522dbda75a99f1f3e0db4046a3dc4c4132678114c051e0`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb755fd3e834f02efea83622543254c015a4203f3a730f75a90cbca87af499d8`  
		Last Modified: Tue, 01 Jul 2025 08:06:09 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f9e25d787b18b8c173e6d09734690ca89fc5382613edbf9097ec66f86e70c0`  
		Last Modified: Tue, 01 Jul 2025 08:08:42 GMT  
		Size: 72.8 MB (72802389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3900e013dbddf97e499b6862d4f7234f1a327aeb1d201a86ec37e1aeebd4e32b`  
		Last Modified: Tue, 01 Jul 2025 08:08:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58e5fcc36be12bc6a887f73d0a37696abfd4e47f345d56b517049caaccf79ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98faac58e2292d5f7ebdfbec17d0be630064cdfea321a1fb300ed3b49343f794`

```dockerfile
```

-	Layers:
	-	`sha256:e5be886ed20a0ff9ba999c683456c2a65ce66541d22b4f162876ac42f10608f2`  
		Last Modified: Tue, 01 Jul 2025 09:36:59 GMT  
		Size: 5.3 MB (5268871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec76cef026b7cd02a973950a337899834aff248c4653728de3c2536b1edbdd3b`  
		Last Modified: Tue, 01 Jul 2025 09:36:59 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
