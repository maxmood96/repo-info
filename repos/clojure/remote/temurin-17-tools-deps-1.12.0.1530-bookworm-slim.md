## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:610405e3b5c36423a0c1413cd45bfa50df81c5f487c33639e040440cb3362313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3f3c9afd8c682cc16297876a254c399af3aa902923951248a110f847a89f631c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242323373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a26d80939dd0461eb6f5bd96135aa228cbeb332f773f2b3687c68a4a64d128d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19acf72e1dcdf08db14bdb9179122adf189de759fceae9a670f365c62e0e5379`  
		Last Modified: Tue, 08 Apr 2025 01:36:20 GMT  
		Size: 144.6 MB (144566594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac7c40be0a9a12cca799a449df9b4466dcbfea5e7c40bdfc67d4aa5d56647f2`  
		Last Modified: Tue, 08 Apr 2025 01:36:18 GMT  
		Size: 69.5 MB (69528480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5514c3764bb5fce7df1b4ded7f02ef6b85a0396be12066d6656968e1d13ecd7`  
		Last Modified: Tue, 08 Apr 2025 01:36:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e2e5d9d15d116f4a0b586d85b7fb9a8c123b81bb95054b4a63d31364833a2d`  
		Last Modified: Tue, 08 Apr 2025 01:36:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a209753c446c6ab1ef1fef6d574ace7b8526c1bbad674d112bfb366045f934f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b920fe7522cc3e819ec353613aeb17df7b5f53e6f51be533c2d8c692e1e9b69`

```dockerfile
```

-	Layers:
	-	`sha256:8c6756a05ffbe79346e2ae446ba458f91459a38feb989c6ddfcb164451b7f463`  
		Last Modified: Tue, 08 Apr 2025 01:36:17 GMT  
		Size: 4.9 MB (4913965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71469a4961851768ab75db5106ecdd8a6ab6503a500ed11ee0a6f4ce46c24503`  
		Last Modified: Tue, 08 Apr 2025 01:36:17 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71f92550181745b9e8e4aa1141a942ace64a98e7b36699360e913d8851769026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240877766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204026261f801ce6a85d003d0d4211d6baa05e9e1f736a692dd85e222b429d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dfabd29c0f6eabe9090686cc1ad0a4bf8f02c0ce0ebacc1f8f57362aa176cc`  
		Last Modified: Tue, 18 Mar 2025 00:06:31 GMT  
		Size: 143.5 MB (143454716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e97676a0436dc28f0aead91cc45ac6e03ef1dd91c1a8101fee1b2073eeb5e2`  
		Last Modified: Tue, 18 Mar 2025 09:17:59 GMT  
		Size: 69.4 MB (69377974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ec8d7bb8ca33fca386ef2cb43798eabc1bbb4524fccd0aaf4d15624da63b6d`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972147c34943f487a71013fbb21960855a55500fec7fda8633ae1ed09981a205`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33b5b9e4272c28bb794b2e5ad7a62167268f7eef82e3699a88bf32a1e0d56155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b01765f412539cc9e936b575abce1becaee394605ebdb5b3dfaba4db09f00f`

```dockerfile
```

-	Layers:
	-	`sha256:ff0a59c6c8ef67713b3f87611e985426a3f608191d9dbd5e3844ebcbe5776e69`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 4.9 MB (4918358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09eb347e928ee8e842c11642e55f26cfaa99dd53df7ac2115db4728f8ab59006`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
