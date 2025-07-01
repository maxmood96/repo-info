## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:8c4a80d751128df1dddde1fbf8d62207fbd3613ff8b9bfd10b2132fb60ac211e
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a9ac969ef56af46777f1a7a0dbe446326ec2c161fb089ca06455d7726139f9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243628618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a14d8e6e4da33bc26b757ec6417678230ec51debe2d606a57d251bfcef901b9`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
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
	-	`sha256:9851a8240d92395a99e35175026ad70b4eb50fb4e03132b209af1bf02a1fa307`  
		Last Modified: Wed, 11 Jun 2025 00:37:24 GMT  
		Size: 33.6 MB (33580925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8377377bede903bb6ac36c3161d53fc83f853abda140daa1b427b70389f3b43a`  
		Last Modified: Wed, 11 Jun 2025 08:18:28 GMT  
		Size: 132.8 MB (132810537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b62dee478970474e4cadda4e3d1b517335fab33336994cfa82bde0e435f3dfb`  
		Last Modified: Wed, 11 Jun 2025 08:24:17 GMT  
		Size: 77.2 MB (77236511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d896658bd59e93c13d90638661aa5fdc4eff0c3bb28df29fa072754e0b1166`  
		Last Modified: Fri, 13 Jun 2025 01:01:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d7c014951abf8b344b837d9cae1748477bffe11f0ffcbc48de5bca96e62ac994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d839d4e6acf37b5032b7b7f4a00bf5c995a1a28a45c4e2187167fdb5da1a24`

```dockerfile
```

-	Layers:
	-	`sha256:4e06efd09e93bf2b394a3728c28fd6e80434dbae3df78a2b6936bba3abfc11e6`  
		Last Modified: Wed, 11 Jun 2025 09:37:01 GMT  
		Size: 5.3 MB (5276695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d1dbf590f37b976fb55fdf2c32c5538e4ee14a9c87deb1dc896134c404cf22`  
		Last Modified: Wed, 11 Jun 2025 09:37:02 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

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
		Last Modified: Sat, 14 Jun 2025 02:34:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

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
