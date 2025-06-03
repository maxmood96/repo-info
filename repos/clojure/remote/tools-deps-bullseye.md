## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:96f416ed9ee711b862ec7f9dcb45715e297a7eafdded5e96dd269ec436831b04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6316db6797f02c9dc90d75bbb07fdaee33c1cccdfa1fa8f228496026e7bc8374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280795550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694268f479f3bd876b27a791839fe682affd9111587563698f4fa9796d8c455c`
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
	-	`sha256:0aa3c0578c3a59a8a3212a55463d1179d9abf668f220248eaea43297e31871e4`  
		Last Modified: Tue, 03 Jun 2025 18:41:31 GMT  
		Size: 157.6 MB (157634512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ef3fffb136b7f5576e79067f26709833b18ca7dfa386fab3bd44a6e230a7c`  
		Last Modified: Tue, 03 Jun 2025 18:25:09 GMT  
		Size: 69.4 MB (69409805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f687a16a7f370217666070ee4b8fe504c76a025203041c0089bf6601755d74e`  
		Last Modified: Tue, 03 Jun 2025 18:24:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94b12950e083af33ddc783ac62db4b0f70df8f4f51ed7856f300763f76213f`  
		Last Modified: Tue, 03 Jun 2025 18:24:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c42efcdd51d74f89c64e6e994ac8354a52ff3521cc01e35f5fb541458a1c8e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7276461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90124e5c07c796011ef856db6b012829d742deaef5dee8ffef4f01e2161db6`

```dockerfile
```

-	Layers:
	-	`sha256:bcf4af94d9a028a1644ef0cae1767917e5b7b22ef6a9d8d032467b71320f4e46`  
		Last Modified: Tue, 03 Jun 2025 18:38:43 GMT  
		Size: 7.3 MB (7259964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7f0e4ed37077519b2fdf4765ec617416004791196f89e2f850566e37bdba7f`  
		Last Modified: Tue, 03 Jun 2025 18:38:44 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a704ff3ce69762dd69d5974947708c470e8461bdceec4770b9a3cf74bc97a9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277708224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f61f54ef2d9c7b564e74659229f3aef74ce4132da62dbbcad55cc87285f037a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a5e26e3cb5abfbd307a69d846765430705dd9214f5910e9a937311871d3dc9`  
		Last Modified: Tue, 03 Jun 2025 10:53:55 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c5d024f07fee3ace22f2593adc9398bc3a987bcd29246281e7bea655a95e7`  
		Last Modified: Tue, 03 Jun 2025 11:00:15 GMT  
		Size: 69.5 MB (69530598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57840e42219844e60d6f6d3c0c076e16dba05aba4cec719ad175d7608d6d3d35`  
		Last Modified: Tue, 03 Jun 2025 11:00:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07eb59a21ffe13daf8c4f1a2041e1a27950fafa695bd1ed9af429f2367de7b`  
		Last Modified: Tue, 03 Jun 2025 11:00:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9811c129d1b082bd5da696898a73f721ce5c3d7ec84da7e705c661405771243c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7281726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31d0bf54e659e20f23bddf4e353f15f9d361223e437e29179c2ff12d306a55b`

```dockerfile
```

-	Layers:
	-	`sha256:394dacea3727c4060e9b7df86cdf5d91940b35233add83cd91cd4f011683b15e`  
		Last Modified: Tue, 03 Jun 2025 18:38:58 GMT  
		Size: 7.3 MB (7265087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75ee34b260ace9ba3e8d51f280dfe75561b9d23143e7e8bdf434607d55c2b2e`  
		Last Modified: Tue, 03 Jun 2025 18:38:59 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
