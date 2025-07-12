## `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:22159a40b217043781128d5112bb319bc5a3681041bcc0cb4869d1367cd2638b
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:95b3f34a53de58daa2dc43b7df7736ef9b3ef9f2351250a9ec2db53476eac59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243400057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1530f9f621840fba36a7c127efe7fdea0ade5a9ba7dc9024f2469a708a92b4`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b63e18595370d6378d79bbbfd5d63e17ff923ea5693877d05c90116a0402cc4`  
		Last Modified: Wed, 02 Jul 2025 07:49:23 GMT  
		Size: 145.6 MB (145635738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d6e26da7d27f02d1c6c3eea06d5e30880306a24c640191103a0e4f413ecdda`  
		Last Modified: Wed, 02 Jul 2025 07:49:20 GMT  
		Size: 69.5 MB (69533532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ac6ffebe545bf491924b50234e532464d68ce83ab3cc5df91e1adcba4cf57`  
		Last Modified: Wed, 02 Jul 2025 07:49:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e6a7db0ea7178c98320599c07c684bc63bf0a7104a787d0c959f2f0429755a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff758db1b51af45a568c6f4d77ad3a106ca6ea1cb1fdba92cc8e451bc7e3187d`

```dockerfile
```

-	Layers:
	-	`sha256:a96e2b022dc897022c2f68568043bbb89756e0cbf1518abc6f10a1d14ca6b41f`  
		Last Modified: Wed, 02 Jul 2025 06:35:11 GMT  
		Size: 5.1 MB (5131385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59851cdc220015c3320cc1fd7dcfb0aa1adfb4420d0d830f1996a0cc4f5d52b0`  
		Last Modified: Wed, 02 Jul 2025 06:35:11 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20c86767d5bb6f7974f9b9ff726db37bf7527ec91bfab089dc81154944476b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239887366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8616cb932c86cb796f6dc00dfeed2ce7ca9eb54ddf4c3b42351afa680b3695e9`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f76e0791e2bfdff1ca6f18c1fa22924455ea225f145d5e5eae7426ebbd04b9b`  
		Last Modified: Wed, 02 Jul 2025 17:14:16 GMT  
		Size: 142.4 MB (142420717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaff8c02f6480fc0cbee01908d6667ead557881affacb7febad6da89d4d1d417`  
		Last Modified: Wed, 02 Jul 2025 12:24:08 GMT  
		Size: 69.4 MB (69388324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8e275893b8b2284d7c50fe185d8c3e859ed71f81c8c884421a4650734a26b8`  
		Last Modified: Wed, 02 Jul 2025 12:24:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:093db83bf2a13453fc07e0442485a05b77ce0e2af74815f85c7d487e501748a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afccda0e60608a52af5851eefbb17004f273e1b74e8d9434c8becb9433cf672`

```dockerfile
```

-	Layers:
	-	`sha256:20e0df9610d6d114bf7c4a81775ff6ab7c85590b0b8472eab672c234b4f742a5`  
		Last Modified: Wed, 02 Jul 2025 15:35:11 GMT  
		Size: 5.1 MB (5137764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c997fe25308c7de6c8687457a2b85ef743d462363ba0d99eef8f45363bf051fd`  
		Last Modified: Wed, 02 Jul 2025 15:35:12 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:17d9022fa5b0d436bd35d1e7951cddf39a00572fac5879374f9bbf2b1f06dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240242308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde80160da37112cfe2e5854e49ad38a0530a1da090c5ea1e7dcae07a122d90`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c46722a871f75a0574f0fd9f3ec3f4f311b1886ecdf65d49f2fb2900dfa14`  
		Last Modified: Sat, 12 Jul 2025 07:50:08 GMT  
		Size: 132.8 MB (132810428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baffec39a25ee99f3c9a62e7deca233376cf27d9e2dbbb86ba0d464aafbad54a`  
		Last Modified: Wed, 02 Jul 2025 10:20:12 GMT  
		Size: 75.4 MB (75358416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc127cd2207951e0a0846d28c93d0310b2774191413921f9ddf950d416fb2110`  
		Last Modified: Wed, 02 Jul 2025 10:20:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:61b4186f0bc25f489226b9f9cdd6fd598218e4188920c672b2b69d90d06ad0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751213cb6808cf6e159e8cef021ede0a5d307f3df7c9e3c6121ecee6458fdf5c`

```dockerfile
```

-	Layers:
	-	`sha256:80401a217a41b319e0b7262c2446108c27de32583f3c967d644bef9dcc30bddd`  
		Last Modified: Wed, 02 Jul 2025 12:35:11 GMT  
		Size: 5.1 MB (5135928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12dfc284515f841a4e748e7b142bc1beeeef5d2496b2868a6236e7a9f2b4f7e9`  
		Last Modified: Wed, 02 Jul 2025 12:35:12 GMT  
		Size: 14.4 KB (14357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1548b345b367949d589db6f6664839473d408f1dde40044248e8a32bd60a696a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220813520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806d0452fd1eca855e81b74fc798f33cd37066554181f2d286f512a3cad423ea`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c9c93094c88fbe81142daba73dbb904cc55b75825bc08064afb1e418f8f49a`  
		Last Modified: Sat, 12 Jul 2025 07:51:42 GMT  
		Size: 125.6 MB (125586082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11d7a457fbcb42fd98eeb09349b488a5370143edda92c1785c515189c77ce2c`  
		Last Modified: Wed, 02 Jul 2025 06:30:47 GMT  
		Size: 68.3 MB (68338982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2816d3ab48dcc4045c13fabc848099abe6ff0baebf320222c068ba32f1dd1c9`  
		Last Modified: Wed, 02 Jul 2025 06:30:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee2d7428e4652c9317647c74cd1453bbc3b7502ed6101e84dfa7a6da7dbc8a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276777d0227c53330b102b6b3f6ffd59e130ae7ccb6198c368c7349f2bbfb470`

```dockerfile
```

-	Layers:
	-	`sha256:998346a644f96261d4ebaed2d48ad7be7ac13aa10daab9cc667c2f9d4ce710fc`  
		Last Modified: Wed, 02 Jul 2025 09:35:14 GMT  
		Size: 5.1 MB (5122710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a018319129bc7d84a0dafc72d2a9156329f00664d52374d6c8de448842ce28ed`  
		Last Modified: Wed, 02 Jul 2025 09:35:14 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json
