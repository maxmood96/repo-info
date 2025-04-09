## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:8c7e9cf2e2eec21d75ee12a5330d9a04241f9c23ef13e6b3fe2cacc0b6b20e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:025d05d2bfe752aa3ce9adb03c72781ae5115043f627694969e5f3bcd8840b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274052215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aff7ce1b97855e3664dd755d9956f00b1561018f5786ccd836c75b46fd481a`
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
	-	`sha256:6a70ec081fbe5483487a649b2193a32f747c470c27017d713f7d66bffe2e87f7`  
		Last Modified: Wed, 09 Apr 2025 02:19:00 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca6063f62af9626250ea617384d610d6dd4f7193172c4d63ac57ac3e2515b5a`  
		Last Modified: Wed, 09 Apr 2025 02:19:00 GMT  
		Size: 81.0 MB (80994108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1348abbf2c827bc8df2cabd08be07677a72939cbfb9cb7cee9854d7cb11d72a5`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b83588ed9a0fe23ef54aa84a5a9c17ca9074302ea903fcab36eeccd62dd68d`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:87f80aa5f315351212c36d678929e27e62291e481a66a7670aace9f8585cf071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7188297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6c203121547a81dad11e2bcf12c024702eb7cad4d9d53203fcf2ea9ec9705b`

```dockerfile
```

-	Layers:
	-	`sha256:827199d8ed49915b5483df2525949e43459bf7a8e16937c1c4621c29032dee57`  
		Last Modified: Wed, 09 Apr 2025 02:18:59 GMT  
		Size: 7.2 MB (7172476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22f28d1b68fb21c3eb25a3513c84589ead2940db84aa10160a533778a73be23`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:760ce351fe6844a39b30a08b05a60b839729cfed8a211a6bc4a3cccac9caba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272625046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa92bb08c62f3cb25aaf465eefd0238fbf691e393995e63de06799f51e456e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e91e8e96d8f5d24cdce2a10001dede19a57e329cfcef9040f34b97b4b9226`  
		Last Modified: Wed, 09 Apr 2025 17:29:25 GMT  
		Size: 143.5 MB (143454606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b8961965d1efefc1296fab27f677a420fdfd0b3928e0b9e9337c8f80382559`  
		Last Modified: Wed, 09 Apr 2025 17:34:27 GMT  
		Size: 80.8 MB (80841928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4054e2ecce0fef24e6bd658e1a769a9465b8bd79784d0ef96e3652885bd51867`  
		Last Modified: Wed, 09 Apr 2025 17:34:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080d15def17660f21ac4321d1325c8780b2bda2a5f1aac52df9eca912b1a51d4`  
		Last Modified: Wed, 09 Apr 2025 17:34:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:17487ac64a6ffbae0b644f17c8beb980efa5ce4cf0c45623064ddb8b5d01fef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41012bead12f57d2ee36745f44e05b4b91ccf127b9744dd05b3f2db2035fd113`

```dockerfile
```

-	Layers:
	-	`sha256:f653849799c128555a9c5d79d0c2e14efe5465e8894d0646237afa9096466fa9`  
		Last Modified: Wed, 09 Apr 2025 17:34:25 GMT  
		Size: 7.2 MB (7178239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c1db99547d2a4d3f214897b38570d415698c4fe78493129485b583f53865ea`  
		Last Modified: Wed, 09 Apr 2025 17:34:25 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
