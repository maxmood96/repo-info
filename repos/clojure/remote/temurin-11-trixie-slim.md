## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:909c6aa2e4f1afd60b881e356666d4f85fb132f0032957ad17814316037974c4
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
$ docker pull clojure@sha256:ae7de5c862f37b39a070dde848bba274d912ecebf8876be411b7abd4140a3dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247601178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5a90a49269667b4caba44d56c3e2fc8bbd1370c50fedbb7fa4b763149016a7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:34:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:36 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c437e6b372d55a33ebc0f4185e2d83a2d3a6634bfe4d1da3bcfd5672e5af5b54`  
		Last Modified: Mon, 09 Mar 2026 20:35:15 GMT  
		Size: 145.8 MB (145806708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfb27266186f65b4fca252ed46d64957b2c8a432e1de3c3549ac67a4c416731`  
		Last Modified: Mon, 09 Mar 2026 20:35:14 GMT  
		Size: 72.0 MB (72015192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16233e3d9c50d68d4756b573dd7b63dc1e2c83e1e866104994f2bf7053db0c5`  
		Last Modified: Mon, 09 Mar 2026 20:35:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d9bdcf7b5dfa4f3afe121cdaebfbb8a5b379630c88af80a0fe5d9e5e7d0d9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7814cd0a80c3af4e685f7318282e5009825798a69807c9b358f3066ce1117a34`

```dockerfile
```

-	Layers:
	-	`sha256:9bfcd552b03a50cf1e288fef8d0587889c871d903db34a14313e10c82e3d25c1`  
		Last Modified: Mon, 09 Mar 2026 20:35:11 GMT  
		Size: 5.3 MB (5279205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009f7840da8ac11292a25eebcda11838bc0acc50a7dabb26698ca0306ae8b1e1`  
		Last Modified: Mon, 09 Mar 2026 20:35:11 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad9aaa37421be6fd8f1eb4104a8faa81796fc6607090ddaa773cc526e76c4f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244474469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df1624a611dab59848b2bff9138d979332cd497e12fe7be129d2f68ff3522a0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:34:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:32 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75258dd608a8853bc52d4dad3936abf513e7cdf09f781c51b390a8827c6251e6`  
		Last Modified: Mon, 09 Mar 2026 20:35:13 GMT  
		Size: 142.5 MB (142501445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2016dc7eeda00ba144837ff26483aa1d462b4508a2120cae6e22c87fb8c12f01`  
		Last Modified: Mon, 09 Mar 2026 20:35:12 GMT  
		Size: 71.8 MB (71832279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41ee085d51bce484b62f9a0d781fe041f9c61081cba63bf0ea9ffbb9dd132e6`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:024e5e130dcdf034f8d616bff14ebc7ff4a204466298bf5108bc7f12b5fc8d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94decf0b5716abe42871f8784337186db9cb457a941dcf6ec4586053a19315c6`

```dockerfile
```

-	Layers:
	-	`sha256:916e42c94dbedb11dfce2cbfdbc3c62ce8f5d39d715731c5bc9b0a0a0a625f6a`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 5.3 MB (5285592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd3305ec451e098200a7626121b17252341aca6fb1f235a7e06fdfaaea1eddaf`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:80d936e6797cdde11df071306170fd0883a1f6a01e2437c2a902ba54e539b5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244027115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa6b07c9ccd74f65d9b1fd61ad0b6f26758c30091eae50d0dcb519e4c439b1d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:49:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:49:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:49:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:49:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:49:21 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:50:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:50:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:50:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0084ef3d4f785d8eed77e52e9b5c15bf9f044cf226f4f0f68abe64aa254ff1d3`  
		Last Modified: Mon, 09 Mar 2026 20:51:02 GMT  
		Size: 133.0 MB (132997823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bcadb16aaea6fa97d2247e88050e85658ecd962ae101b5d66046c14858eaaf`  
		Last Modified: Mon, 09 Mar 2026 20:51:01 GMT  
		Size: 77.4 MB (77428429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2ddd2dec7dfeae62af943793b99fb93af9651dd7190dd2434e943145f0269d`  
		Last Modified: Mon, 09 Mar 2026 20:50:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22189bbb021a548295bd552fa7cbf354402266d013dbf3bdd7c5b5b6de5515ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b166e3c5c84c260998c151ce28aa84a1d7a9ba16be2e044a571c4c42b78f6`

```dockerfile
```

-	Layers:
	-	`sha256:970439528749cbdd44811c3e6cc704e0556d932167a78f5083f33617d1cd4b39`  
		Last Modified: Mon, 09 Mar 2026 20:50:58 GMT  
		Size: 5.3 MB (5282961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbe9ca8a72baf4a6023771995092970dbeeeb31c074b26a07dcfd0b045fa2076`  
		Last Modified: Mon, 09 Mar 2026 20:50:57 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:20a826361d5d623d7b571d3d6f66b62304cc7c7cbbb5b827a7bac8e1d2239a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229384585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffc3a997e79d67072480ce91a2bf21620aebf3490149ca0fecfab48f0868f92`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:26 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f09f9a8868680d395a30962c68bac28d9405a659030c5d0f5c217028209b0db`  
		Last Modified: Mon, 09 Mar 2026 20:34:13 GMT  
		Size: 126.6 MB (126562037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b3c2d48ac51eb278695fc95b1e83fe5700e4c6803159eb52161e92b034ef0a`  
		Last Modified: Mon, 09 Mar 2026 20:34:12 GMT  
		Size: 73.0 MB (72983722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd2c7cc833e919ddb9a61a390588d271c1620f4b922b62d5fa3398b513d5c58`  
		Last Modified: Mon, 09 Mar 2026 20:34:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87c2eba0fcaf81101f9ba5d6ec506517a54df82abbde6ce967d615d6797409ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392e83d6493e6080bcad7c2c22ef0256e263177837b0328a88feb6c87aa85a4f`

```dockerfile
```

-	Layers:
	-	`sha256:1136c9ee30d1b82688e652bfe9a1b4dfbe15332f2968b771491d862332aa4bd6`  
		Last Modified: Mon, 09 Mar 2026 20:34:10 GMT  
		Size: 5.3 MB (5275133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e09333d939e277b631a579deb5226f73d34d3dae86a0fe6fc6e3194353b790`  
		Last Modified: Mon, 09 Mar 2026 20:34:10 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
