## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:178c73fe78b00fc2744c6ee6c7b078923a813cd815359cff6c672896dd80e87c
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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e391029f56033fb5a045bec17d5a6ad425fb579c780da9e3a98c696febec8dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187716799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e47cba383dcffdd245535b8ede85efc85c02e6bd0195c3ca91bb8722e3f28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3613b7ff44e596289d2b0298e16df1c767af112d9ebb57b914f905eb0830143`  
		Last Modified: Wed, 02 Jul 2025 04:17:43 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b6f9c8ebd41b79cce5ebb6e4dd6858f28b2f80ca379cac1d83edaad5c9084`  
		Last Modified: Wed, 02 Jul 2025 04:17:40 GMT  
		Size: 69.5 MB (69533603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb70a8c662d84105f0b8357a59826368fb22517f968d863ab4b122e76341df40`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b833070a83bbe781f33742ff1b46afab7621e9c728b2a13c59614927233351`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b4f41ec2a3331f1d58e8c1081c06303a1629cfd40ad0d8214c0ccd8e9ecd7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca516b45c9b5710d62c92dc7035ebd4b4b771c9620ce8480487a46cefb3f036`

```dockerfile
```

-	Layers:
	-	`sha256:1f25983a7ec3c0f8bc161a441ac4198dc8a79c58c91a5e1fcfb284fba1ad0ee1`  
		Last Modified: Wed, 02 Jul 2025 06:41:05 GMT  
		Size: 5.1 MB (5061890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3909ce15e9446299c9f1e90e2bc8cfa33ca44ee9df7efbcc66310b050ca2c4cd`  
		Last Modified: Wed, 02 Jul 2025 06:41:06 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e429f44766c560be2880552623ddccbebc44ce209e09ce8c97437b14592d4618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186558552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a308d69d67ea4a16161ff3ca01c2818c88ea216016a97b6b649ca0e8a5ff8f5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10650de5699aa14c6dedbbb6c706a301e96916a651c7fd0998812107358f9abe`  
		Last Modified: Wed, 02 Jul 2025 15:23:52 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57b65103ad287aa9ccdfd7e7014bdbd929aa505edd751d662ecf44215f4baa7`  
		Last Modified: Wed, 02 Jul 2025 15:23:54 GMT  
		Size: 69.4 MB (69388559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7c159bc81c25ad32c8c8b3440e2ab3ab99815289e1b21a7caa64961948c625`  
		Last Modified: Wed, 02 Jul 2025 15:23:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b1712f5468dc3cb552d5654b7c61dddd9e455378e043058a17d6a4dde34905`  
		Last Modified: Wed, 02 Jul 2025 15:23:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65392c84d8f480a3c13b2e301078d85069fa620f13f5ded6dee8422683cff371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d180638dd9aec9111c63a081b39e4925c52c128fa197460d2139c356e3f28312`

```dockerfile
```

-	Layers:
	-	`sha256:432ae3507c12e07238ebcf6f64317dd5b3b2213b84ae76afab0ed54cecc867fd`  
		Last Modified: Tue, 01 Jul 2025 15:39:52 GMT  
		Size: 5.1 MB (5067648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8c1c26175a2ea86daf5e2354e7cf5cb09de71a33f8f12bc456444887e885e1`  
		Last Modified: Tue, 01 Jul 2025 15:39:52 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7a8ab282786e7aff74cabfc3854bf88ac014f0c982b7559ffa218a023d78a514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197352840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067c151e84bf0c714d918e0201ef30ddf57dee0308fb0794c3602e3d1748198a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d324dfe17bdac3152b73b6635cc84a3cbd63edc899e737aba818b7869d073ada`  
		Last Modified: Tue, 01 Jul 2025 09:11:13 GMT  
		Size: 89.9 MB (89920247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15b7e53c0a0a07c0aa482f12e316af3142445cc7d65e4db454413bbc9760853`  
		Last Modified: Tue, 01 Jul 2025 09:19:00 GMT  
		Size: 75.4 MB (75358732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dbc5632f1ba52e2c86bebb057fddce545780249a3404f28ad11310ba9d8db3`  
		Last Modified: Tue, 01 Jul 2025 09:18:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0d8391a5ebb0e57168887bbf1046f683521a863af3713df771caf06d0a0402`  
		Last Modified: Tue, 01 Jul 2025 09:18:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:66f3664d0af2c6d267421b4aff23c4e49b031e9385eeccb04cf12688e6fa4be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12570deee4784c45d99ad9775b3cfbee61e5fe69ac7672e068d1de2da52bae38`

```dockerfile
```

-	Layers:
	-	`sha256:0724dc2f146ff69411015772a95de2c72e3510c8914265849221faee49ed7871`  
		Last Modified: Tue, 01 Jul 2025 12:37:20 GMT  
		Size: 5.1 MB (5068346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c537b818e4f3606407ecb5f238ca12537a09496cdedc2cccb30e37eed599ab4`  
		Last Modified: Tue, 01 Jul 2025 12:37:21 GMT  
		Size: 15.9 KB (15919 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:751899aec45c0fd94f936c490aa63b7b95c95c59231822123c56be81bd82b3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180444263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4763842e28f16c013a917d386f92a7bb47b69ccd9e15c89bc27a21cca8d470b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f04d395d125fbec228c757e4d9d00b68bcdf3d9f3aaba3684b8403802ee00`  
		Last Modified: Wed, 02 Jul 2025 06:57:08 GMT  
		Size: 85.2 MB (85216779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840ace56d51769d4ced2ee3aebd4459b5043cc380030b7934967cd20f7e5119`  
		Last Modified: Wed, 02 Jul 2025 07:01:47 GMT  
		Size: 68.3 MB (68338634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2eaaf828fa5c853d4a247595071f1447c9eb90b0df68e6fda33997784613b`  
		Last Modified: Wed, 02 Jul 2025 07:01:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026ece8fbf4be5d0ea126eb7bc7d72ae7c17863d014aa9d6be1df9698926398`  
		Last Modified: Wed, 02 Jul 2025 07:01:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1449fb1bfc4262e4ea28b4f6acf4e0a328fa8de53197e04cdbe5e4ce9bbe1722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f719a78febe87789c892ae7d1029fa5b4be9876b9c40f543108d29fc838612de`

```dockerfile
```

-	Layers:
	-	`sha256:16fcd9077067486b61a7b4ea8d7e95b76cea66a00e31fceddf679c3b1c448c99`  
		Last Modified: Wed, 02 Jul 2025 09:40:37 GMT  
		Size: 5.1 MB (5055759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c5ec97c8de181ab7dfda9771097ecb94860676c1ea5edac3ea4faf9ad0996e`  
		Last Modified: Wed, 02 Jul 2025 09:40:38 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
