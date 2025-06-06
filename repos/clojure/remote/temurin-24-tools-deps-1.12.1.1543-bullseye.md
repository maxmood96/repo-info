## `clojure:temurin-24-tools-deps-1.12.1.1543-bullseye`

```console
$ docker pull clojure@sha256:d52ebbfa1a2dcb28ed70e7d97e5f7b669ee9337498c698de8ff8890e509d798e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1543-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8c59172874db89fae153a55455078fb06b919f8d98aeeaafc42444c7abac7a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213113279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a93ae3243323e7e3fc609b477d4cd3c998280becb28a36db6fbe96d3b9abda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc5e4135ee581b0aa3247eaa73ca7a69af63af36bb774e98902afbadb93313`  
		Last Modified: Tue, 03 Jun 2025 18:24:55 GMT  
		Size: 90.0 MB (89951990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d4a984155e232763d150013559fb65ae5c9f024f6951adc1e081a785fea66a`  
		Last Modified: Tue, 03 Jun 2025 18:24:52 GMT  
		Size: 69.4 MB (69410053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397b5e561d94f0cb61c50d73c0e1b342490ad172a3e61a4b40e57596a0a0df5f`  
		Last Modified: Tue, 03 Jun 2025 18:24:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7023ab0472d7d3b7aa9098ab18dde36da2ccdad24467d23d608906651d1eb590`  
		Last Modified: Tue, 03 Jun 2025 18:24:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8a8a9355f2f9d721ce7ad443636f2093026d8499aba3a87c90d872938fd253a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6d977d8a39d4b3afd37c1f52cf54efbee2d844bc5863050d34c29d56bdce40`

```dockerfile
```

-	Layers:
	-	`sha256:2d389323d8e06333fb1823f7342a1ee719f058502dedd584a7fe3a227feeaa13`  
		Last Modified: Tue, 03 Jun 2025 21:42:35 GMT  
		Size: 7.2 MB (7206832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3087e8250543de929ce766e59b4c89670ea34e6c956f25d8534ea7780434f6bc`  
		Last Modified: Tue, 03 Jun 2025 21:42:36 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1543-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05a7636761a59ae86c3c4c261307d831865539db5e26e379550f194f26936940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210878155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c737ed9ef096981495ed220a3a65ddee2b01cd334108a084fc85e51025d39450`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138a1071d10d13cb8382959f5fbc892b4601755504e76a2d09f248081aa2606`  
		Last Modified: Fri, 06 Jun 2025 02:47:11 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c770de9e6a4ab2cd5cee09cc3904983212a383ac48c2f534e3f94eb72657a2`  
		Last Modified: Tue, 03 Jun 2025 18:53:54 GMT  
		Size: 69.5 MB (69538087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb415c124b7df417f0d03fe1c7f762c064dfd1499a396aeb9b8d61106fdb01a`  
		Last Modified: Tue, 03 Jun 2025 18:53:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37b9d4fbaf08505fdfe6951df9a215e8319b522ebe1a2e2612d1bf89611dc34`  
		Last Modified: Tue, 03 Jun 2025 18:53:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1543-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b877fb29fcf4627918a605af758ce1c6d437fc8f23836259fb150173f405110c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627857ef8f02e04acaa61e3a93fd401c50172c2233b7796764a78e48916e2a61`

```dockerfile
```

-	Layers:
	-	`sha256:8dcd057d3840448a5bc193b31368509301338ec7184a4076313637890d408b15`  
		Last Modified: Tue, 03 Jun 2025 21:42:42 GMT  
		Size: 7.2 MB (7211928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497963a44df012fb8c92f672a2be20ec6ba25a65bbfe4c23f706f168abafe3bf`  
		Last Modified: Tue, 03 Jun 2025 21:42:43 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
