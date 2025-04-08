## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:fa50a02fea5afa578c22c023121d39870ab911d2a655870db0d0c1c5e1ba48c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3d57eebb8b2fec2b2d72222583f9611217a558eab213be9fc9179bceea8b80a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274052236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733a9bf4f79de1015ec2a248641de18527d469a4b6a114a9f1b2172218d335df`
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384928da5074ebbb01e61be8084d664629974b9f4e2c65abbf0cbad3448967e1`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 144.6 MB (144566556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5180520d2d9e9bff3b74f840c9b797063d31a2b38fdcd556e3196e984d3044`  
		Last Modified: Tue, 08 Apr 2025 01:36:25 GMT  
		Size: 81.0 MB (80994098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5205c2cec2b37669ff76e2abe02fc9a88361bcd27e93ce9363bc40fe6f379af`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbe6a58d39d861e8ffaacd28d890442d96e0a2245d3fa34a475908c571c199f`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7829e123c989e267f7263e7e2685a9073807b68ce6503a7c867c4ef4b062c166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7188297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf08d009bbeeb1e48bc68c0842f6e800e65f9d041d8d0c3baa2027752956e3a`

```dockerfile
```

-	Layers:
	-	`sha256:3f65a9a9ec4dd61e56adb178128121d4668c45ee6605c0ab980319e9449a8766`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 7.2 MB (7172476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d91a5075a49b7d91a115666fcec39a0373fc0a1ebfaef8c9ebf790326f5932`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80f7c0e4ca0914a04c2af75ab5637ced541d7b671175e2d70056e1533be205e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272603411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc12dbc15a02e135e3d43e197c213e07d3feaa01816ac8b8018232e42302f8`
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998164cfae4d7f81bfc93eddab66e4a630e0ebbdc2a82ffda297a99017b6aa1e`  
		Last Modified: Mon, 17 Mar 2025 23:40:16 GMT  
		Size: 143.5 MB (143454716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719ec5c6f685922819e6ad078067d97c7503551d877000bd6b826069be0543d3`  
		Last Modified: Tue, 18 Mar 2025 00:02:37 GMT  
		Size: 80.8 MB (80842796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3af4718ea050154c3a88839bb48844f7c8655f9cfecfcacef4d0029e0d680e`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd44b4c7c94085fdfad20f7cd7391304a446f7035a2732d14443613fa61233`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ad45d5b0912c732c7648c36bf23a68d2c3224fc4d391c4a4da1f8f5172228208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb84681039560de16f5c698947b6694556ca668250bf04062cfe3e0f781d171`

```dockerfile
```

-	Layers:
	-	`sha256:8859e5ff191047d1ed53892d7bddb0ff375555fff786d43f4ffe5cd03a685506`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 7.2 MB (7176871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:150b8c1d4a8e21d6b42ac754a87e30b9cadb673679228472dcd7e3640bb95bc0`  
		Last Modified: Tue, 18 Mar 2025 00:02:34 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
