## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:9577c41ef7f70bfc2ed0aa3f55e5c452a287a7f42c9b06c294a707cce84d0506
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

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

### `clojure:temurin-21-bullseye` - unknown; unknown

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

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4cc964c38aba47e124d2e36687977f50bd2c44ef219aa8e0728a0579e788898e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277715437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dc32d1b050c76b451f47ad2e9ff8cdf1219e579264310443f9b9248107635c`
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
	-	`sha256:34a5e26e3cb5abfbd307a69d846765430705dd9214f5910e9a937311871d3dc9`  
		Last Modified: Wed, 04 Jun 2025 12:44:46 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f332d8441bdcbadfb908719e2d8cbab6ab21491c9920c839452b2754b865dbd`  
		Last Modified: Tue, 03 Jun 2025 18:47:17 GMT  
		Size: 69.5 MB (69537810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382be28f229b33afdc9a2fa6e9b631eba685ad251333a98fb98131550402e7f8`  
		Last Modified: Tue, 03 Jun 2025 18:47:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11061d96d15362845641bbdfeab3c811a8f72c9746b42dbdc26097bf8607a3bf`  
		Last Modified: Tue, 03 Jun 2025 18:47:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:85fba926a0d21485ca480dcbd46475acdec307892b00558d19c380cf85ffa575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7281726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66376ab5210cfd1f721b3ef950abed88e3330fe0be363ee465b228e4cfb19565`

```dockerfile
```

-	Layers:
	-	`sha256:108961c3af75a30999716cf8181447175eee13f62aee644906e3e9e20d02c0ed`  
		Last Modified: Tue, 03 Jun 2025 21:40:06 GMT  
		Size: 7.3 MB (7265087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1482a6185e160b000d0a4ebda21cc1ab80cd735236dc96099eaa979771a21bc`  
		Last Modified: Tue, 03 Jun 2025 21:40:07 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
