## `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:7c63dc70e0bfae5fb2f71c8808956f1f4027e881492acb2cf4ed9273bc089f3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1cb9f183d4f6b55cd880d472cbcaab8c13f8b00a9d2eabf7fde92be4e16b8f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.7 MB (282685819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ef570e0c1f00af3ecbe4b70470d53bfa247368c3bf6984ec2f74af59355906`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bf5b3ef0ec2abcff9c85372ee7df6989a8a6a3da0c30828dd60521e89406da`  
		Last Modified: Thu, 25 Jul 2024 19:05:48 GMT  
		Size: 158.6 MB (158579313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1b3fe33fefb22590b890fd5e7ad4426e2aa1e6cfec63e58b378692cb99e97a`  
		Last Modified: Thu, 25 Jul 2024 19:05:47 GMT  
		Size: 69.0 MB (69020885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b748068185149157b0895ef91e4c64c279cce202e266ced2814dc8b450452f`  
		Last Modified: Thu, 25 Jul 2024 19:05:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28cba71e5e70ca1ec1f41d47d811af31072120f271565f4603c99cf0593a50f`  
		Last Modified: Thu, 25 Jul 2024 19:05:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b0bc12edc19bce4f00b5161dfa6e5fd7d247a3a23df604fa882ec349d5ebd7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64885a1c17152cee041961c9cdf99002b328bbc22e3c26b6eb3c502e4bc85ebb`

```dockerfile
```

-	Layers:
	-	`sha256:5b003711a0957859e0f66f4ca249faa48f2a7b28435d783d54bef9247d726d87`  
		Last Modified: Thu, 25 Jul 2024 19:05:45 GMT  
		Size: 7.0 MB (7041030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15153a74d11691a3383c751149f8eda2c4663bec607290173981802ef189cc5c`  
		Last Modified: Thu, 25 Jul 2024 19:05:45 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:400d009b19ae8180b4656e0bb541806498347d00a35f5c4d4b4ceb09766c21db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279611099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a986aa3a29fc5a4eb49bc8a6e387e3a9207cf58b2c668a28c158fae2dd5f290`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430d84b3203c6622dea811cc35b3f4c6b527003ba6199fff9466c03919a6664`  
		Last Modified: Thu, 25 Jul 2024 21:17:29 GMT  
		Size: 156.7 MB (156746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b7743aa85df4f41c80829464b6f57e2d1e059e8c7a4f45de4694c0c8b94d2`  
		Last Modified: Thu, 25 Jul 2024 21:23:53 GMT  
		Size: 69.1 MB (69133890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096f4fee4bfc08b085874e77ad631e369851e9ea35c5ccb0b359df84604a8062`  
		Last Modified: Thu, 25 Jul 2024 21:23:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba591eecf4b4da141876a2ac06d31c80fd267b64281fc820fe5fea49fb20c4`  
		Last Modified: Thu, 25 Jul 2024 21:23:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8d05584c28945e3455457901a0543196b67c1f1c14444870b4ea3be0983a0c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7063452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa068f9dfb8d3faad6f2cbf13ad08073c72cb47d24972faa937f76faceec8d7`

```dockerfile
```

-	Layers:
	-	`sha256:dc2d94f51e338f458c6677aee0129e582aff6ffcf864c7f7688693ad1d5d7024`  
		Last Modified: Thu, 25 Jul 2024 21:23:52 GMT  
		Size: 7.0 MB (7046776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01c31c773e7441f1ed92dd0624eeb766667ba94213cd94f945f92fe42b63e46`  
		Last Modified: Thu, 25 Jul 2024 21:23:51 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json
