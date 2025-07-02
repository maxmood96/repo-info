## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:ef76c29f730d510bde27290013579f8a2f252e34557b30bbc59d83888c952f8f
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25dba85e019194d5b0269148b4fc7ceb66771453b8bd4604b0a7a742d59a663a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239887505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4996b51a004d5b5667ba35ce9b8a0b7cfbb0041e4d55adabd77e1c847347af37`
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
	-	`sha256:dcc1d02c448fe485425583bcbc9b5e3bd61a6bf61836f73f72aced0d452aa9c2`  
		Last Modified: Tue, 01 Jul 2025 13:33:05 GMT  
		Size: 142.4 MB (142420687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de979d126f806ab608fb5a5f629b6dd90444ee3eaeb0b71aaa679f8bdee1732b`  
		Last Modified: Tue, 01 Jul 2025 12:12:01 GMT  
		Size: 69.4 MB (69388498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb82171284c7267c5f62f326dec71db00d2cf87253ef7725c644204f709e32c`  
		Last Modified: Tue, 01 Jul 2025 12:11:55 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:406bf8ae29f112cdb4f7f4437c5b1b7f63deeefdb5cddd13f5cbee49e2436a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed55727beb42a6e26d9050468b0e26c588ad7017f94eb13b0136df3c282c03ec`

```dockerfile
```

-	Layers:
	-	`sha256:ae0aa2fdca18e71e9d626aef1400ca7f6ef7ae9d09fe07870269fab3636ece95`  
		Last Modified: Tue, 01 Jul 2025 15:35:11 GMT  
		Size: 5.1 MB (5137764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b1a7267b29363bbaea0cf9ccd54e14f416ff3e7a9c17d69899881b3fb5c5a7`  
		Last Modified: Tue, 01 Jul 2025 15:35:12 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3acffcd7c4570e16b593dc2093b465408b9add0b26c1e338b176eac082057f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617bcdd4a196c55e52df56e5851af059cfaed65cd043cd1771cddc95a9284856`
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
	-	`sha256:b02a4696a1589b7f993ec4c3885ec710d9efc34062e9aa63943ba38857696a35`  
		Last Modified: Tue, 01 Jul 2025 13:32:41 GMT  
		Size: 132.8 MB (132810523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa598e273687829f5c652f9d14dbcb0f012201c3c0950d4b425550c18460e6a0`  
		Last Modified: Tue, 01 Jul 2025 08:37:16 GMT  
		Size: 75.4 MB (75358028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11ffe1ceebf7241b4057af65c130f6cd176ec66ff2de5b7eb1f382b70fafa8`  
		Last Modified: Tue, 01 Jul 2025 08:37:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8cbce389eb6beafd03eb6368b0eb2b23491ef5eeeb18715610565b155624aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d9e23b6040a6eb1745cd5b49e136b515158dcd6ad019025238a81d8be3e3c`

```dockerfile
```

-	Layers:
	-	`sha256:eb71d5f1e00a96e39b5f258cbef3ef4a081bbb3c446c65978ff6d6ab88fc4a5a`  
		Last Modified: Tue, 01 Jul 2025 09:35:40 GMT  
		Size: 5.1 MB (5135928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b09548efa35e9b2021f4d5655b4df95c6ff3694677633e74cba209b413c0e7f`  
		Last Modified: Tue, 01 Jul 2025 09:35:41 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

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
		Last Modified: Wed, 02 Jul 2025 06:24:58 GMT  
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

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

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
