## `clojure:temurin-26-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:24f58420906fd4b63b1fc58c05e2b13d1fd217c0e85d5e5e27d297887faaeb8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:34b375331d04e37e8bf3cb69bf06c008fa35383a7f09fe0281c866fff2e2c0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217817207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457ca26f619a3f837ab488ceaa00d727f2f21032fb3510d29b7cca9c4a062a62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:22:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:19 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcda5d39d379c60b31dd9ddd9104c436e9b0e529d066197aacfb6182efd9972`  
		Last Modified: Wed, 22 Apr 2026 02:22:53 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dcd306efd69fb26553e2c4e49474f64c8c2b48f2e3e9bbcd0d9f1ab309669f`  
		Last Modified: Wed, 22 Apr 2026 02:22:54 GMT  
		Size: 69.6 MB (69597327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd5e8b3cee6e90112a4a84bffc7ac9366fb3f9f0e533013f9ac65f846e97d04`  
		Last Modified: Wed, 22 Apr 2026 02:22:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e45fc1bc57e7f580f3f22c257a57d2d3127fe54904d766edb3c1437d75e3ca`  
		Last Modified: Wed, 22 Apr 2026 02:22:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aaf170f991584339df684a07b09983f0f1d8bbc5bbe662af8586a4f35c9288f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac2b58cc34dec7017e07e7f5e5aedfd920adfd0c257ce66021c9947dcf172f6`

```dockerfile
```

-	Layers:
	-	`sha256:a6074d7ccdd79f79d1232336ef0b04707fa221b1be099868fef4315f8de7b5c8`  
		Last Modified: Wed, 22 Apr 2026 02:22:51 GMT  
		Size: 7.4 MB (7373157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23df3194027254bb9ccb0a2b4d34ff8824fef05370dbe2a3d800a2062cfaf9e`  
		Last Modified: Wed, 22 Apr 2026 02:22:50 GMT  
		Size: 15.8 KB (15771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cece7e718df71564747b6defe8228693074ab763533a1b289c7bcd6c221b01f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215387729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd04772c1a1fe7d2876b4102f9ae36166978c067c9014fde2d30782bc39f9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:25:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:25:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:25:09 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:25:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:25:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56be05e18c5d9b4cc9a6a882fa03b8a740d9362f4266f03e250245a28a24ec59`  
		Last Modified: Wed, 22 Apr 2026 02:25:44 GMT  
		Size: 93.4 MB (93395213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d103d1723061f8bb1111bbdb89c97075c2982d1abd0a5f3539ed211df7a751`  
		Last Modified: Wed, 22 Apr 2026 02:25:45 GMT  
		Size: 69.7 MB (69738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217872670154886c812adf490fb3d8151953d86b4083ed9d9c320dd7ceab606d`  
		Last Modified: Wed, 22 Apr 2026 02:25:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da00760cb8acd4d78361b40bc2c352e90565121db0b41c8e652f014149eabc2f`  
		Last Modified: Wed, 22 Apr 2026 02:25:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:17590c2e0da302aaabf32f47cec4791f3f9fe4a0fc1335ffff284332b97d51f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189c04cf017d7c68d93e95151ad2631b632bc385503c59c2f473ba1bd074f523`

```dockerfile
```

-	Layers:
	-	`sha256:2fbd58ec1c1356d8d0181106225e399778d4e5b532c7f64d923f581def97eede`  
		Last Modified: Wed, 22 Apr 2026 02:25:42 GMT  
		Size: 7.4 MB (7378253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34850c8e72b96de2cba296ecf658785bb855e717a9d22d58e3d02737b2de885`  
		Last Modified: Wed, 22 Apr 2026 02:25:41 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json
