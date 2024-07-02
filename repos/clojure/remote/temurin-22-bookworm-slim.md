## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:5277ddc5d738ceb075ddcf90e992b5ff3342c946a175ac79ca3cc64a82010024
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:09734dc2267874ea9f99b5c6883d2a311c3cd9a714527e1b0a7a24776b23473b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254909242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5c60565b415b27cca07bb3c34382d1cb9d51f9147054382706892ffc4aad8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5ea8a4f2940abe800c186801c5340f0578d663e0cda95a38d988cad20ffae4`  
		Last Modified: Tue, 02 Jul 2024 07:09:19 GMT  
		Size: 156.7 MB (156715497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c583bfbf58ee7b6eb4e6033847b13b8d582799747c92f287afd36ceb45287f`  
		Last Modified: Tue, 02 Jul 2024 07:09:18 GMT  
		Size: 69.1 MB (69066424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f0cb8bb74dcb734fdf2421530234975333bb0f0910f1e486808e422511232`  
		Last Modified: Tue, 02 Jul 2024 07:09:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ef0018284e91ba9d9d39e75e21d2cd646d233961ecbadeb0423baf1f2298fc`  
		Last Modified: Tue, 02 Jul 2024 07:09:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6006c7e3b5f252e7b6f82299f8deba47d1079bd34b679d8cb88f8f5a540c5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db69c2a2a62456da76a5bc4978363323b1a44f8927cd2eb8f2b6ee9682120c5e`

```dockerfile
```

-	Layers:
	-	`sha256:69ba497b3abc6a61c12fbdd3a8c6ca76b197cd3a3e6cb6936b2cf1b245f5327e`  
		Last Modified: Tue, 02 Jul 2024 07:09:17 GMT  
		Size: 4.7 MB (4705033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1bb0639cc0dd5252c36c6be4025d7fb7aa3448d44bf896510b51357e7e76014`  
		Last Modified: Tue, 02 Jul 2024 07:09:17 GMT  
		Size: 15.5 KB (15511 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f476ff04c11b748ea29fc41a330920ee7aef8a6fa941e73fbc1a943e143ad85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252714101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e025c416fdd4ad3f63ddbb1154d4d755a237791e5ee69b5566e5ae716ca425`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db123f60414e6579afa1a9d6b132dd9867e08b53008118b0883aaf2db50b2e7`  
		Last Modified: Tue, 02 Jul 2024 09:44:24 GMT  
		Size: 154.7 MB (154737984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8296f44bfdef8deed69defaf61f3ca7cbb710f1f3229bfd5727b838a2674d57`  
		Last Modified: Tue, 02 Jul 2024 09:48:32 GMT  
		Size: 68.8 MB (68818514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9395b81f794779455018ae9811fb36d007690b145e14d49ba543755c120ea388`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911c622b042c8bf9ea71fcd0b9391a1aec469f24b2ba32c69d50feec842dff3`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9570e779d186c7de6e5ae1831099ea4f539339f999cc14ca2e5aede7b4ad662e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c1d770a07bb4c0ab9f04d511da9736790a44806a34a3ea3e661a9161c9e269`

```dockerfile
```

-	Layers:
	-	`sha256:066a063d42be04f90bb221bc22776c35932957dceb1c18631748341fb636fef7`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 4.7 MB (4711418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7f923e1e8ba8f822ccd65fc2940f48ccb1e2708afe39da6ced2ba9c933818e`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
