## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:1dfe75cad37d1b8a5f41beb7e66d439b931944e5aff40cec425533f660be883b
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
$ docker pull clojure@sha256:1ad4955c7674b3533f31444491caeb755747cd491c451bfd8dca6b55e6d50ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187716832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c80c7bbd11acd0ba5ec56bce3920069ac5b32b5786d7bbb2d484b26103ebe1f`
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
	-	`sha256:d08b6c90679f0c47bae60c2b1bb5af7621a7094f4b06b34679e542299b2a7a90`  
		Last Modified: Tue, 01 Jul 2025 13:33:04 GMT  
		Size: 90.0 MB (89951991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287a209e036893c65c88fd5f2c9437f1165f03fcf919dbcb88748b1a5c2d50a4`  
		Last Modified: Tue, 01 Jul 2025 13:33:20 GMT  
		Size: 69.5 MB (69533659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5aaf96a9e9e0f5b97805a250704ebdda7a1d31775bd6246cdc7e2d4067df6`  
		Last Modified: Tue, 01 Jul 2025 13:33:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176b42d5a00fc85a0ea676bd5b65197b3e5d0081187a9b8090959f9fff3de460`  
		Last Modified: Tue, 01 Jul 2025 13:33:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1994fc285860cf2505e7b5454868652341c55b3807fa749414c5738b9c7dded7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475243b7fddbd35b22ec4cac97cbe5b6b334a4a066dfdb74fa17cdb590aa565`

```dockerfile
```

-	Layers:
	-	`sha256:fc5bfb0134a81fb5f31a1d85f808f7df61a026fb5c7829a52a11611bc7a566a4`  
		Last Modified: Tue, 01 Jul 2025 06:40:19 GMT  
		Size: 5.1 MB (5061890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6457ea6237d05b7551a9f605d02848230f11caacedc9ffb0bf649bd3852de5cd`  
		Last Modified: Tue, 01 Jul 2025 06:40:20 GMT  
		Size: 15.9 KB (15872 bytes)  
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
		Last Modified: Tue, 01 Jul 2025 12:37:23 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57b65103ad287aa9ccdfd7e7014bdbd929aa505edd751d662ecf44215f4baa7`  
		Last Modified: Tue, 01 Jul 2025 12:42:38 GMT  
		Size: 69.4 MB (69388559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7c159bc81c25ad32c8c8b3440e2ab3ab99815289e1b21a7caa64961948c625`  
		Last Modified: Tue, 01 Jul 2025 12:42:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b1712f5468dc3cb552d5654b7c61dddd9e455378e043058a17d6a4dde34905`  
		Last Modified: Tue, 01 Jul 2025 12:42:35 GMT  
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
$ docker pull clojure@sha256:024ab3788f443827e1a29b367c48cf781b86a06b6824e8c9ba85c650f9abf828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180444354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f07983a28083cafe1208aef011e650ad94ecaf5b18f0b9d9892bcef0f20857`
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
	-	`sha256:49b2bba002bcec4c335f678daa4db55f8ec58480561f0b4815e5436d1584f634`  
		Last Modified: Tue, 01 Jul 2025 13:32:57 GMT  
		Size: 85.2 MB (85216805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd75503737876f20b8106974407ba5b904c129e0ace4ffb9e99010c81aa25d9`  
		Last Modified: Tue, 01 Jul 2025 08:29:58 GMT  
		Size: 68.3 MB (68338701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013f6eb20aad271c675bb74800f6234216566ee043cf9261a838e5b702f2e767`  
		Last Modified: Tue, 01 Jul 2025 08:29:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ce34bc888a0f4efbccd66d5f4122e1f997b07b75791617b802fd1f2db7bf3b`  
		Last Modified: Tue, 01 Jul 2025 08:29:54 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8c4c8ee1b66c454c8d1b526ad4553f44fdd56799baa64b12d158bd93a02b803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cf85f8d2fbc6b336861e47ca1945583b5d3126cebe45cbf06f8732f50e6d93`

```dockerfile
```

-	Layers:
	-	`sha256:3af336132d1d5bc9077c999124164871ac5fa4a85039f4e77ae84eb626bb84e1`  
		Last Modified: Tue, 01 Jul 2025 09:40:42 GMT  
		Size: 5.1 MB (5055759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9cfec4c2a7fa3d1c35e31d56a4c1059e07b387f043eca2bfbbc1d096facab16`  
		Last Modified: Tue, 01 Jul 2025 09:40:42 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
