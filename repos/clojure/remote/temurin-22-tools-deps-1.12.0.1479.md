## `clojure:temurin-22-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:f4b74942930c99c38ca6398897691d9216f2acf910720fb9fe99093d054b09b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:4b9dba78642b82e4a756fcc94da061626a5cf1f7fa3008d4342fe9799a41ea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286738145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0143e4bc49707a28bb855bc640905cd1eb8fec93e8b987fed82ef5eb6ade8bd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6f3d200912b3cf82d5f6da9220f86b82a57c4e5469a85630f36c12eb3d16f4`  
		Last Modified: Fri, 06 Sep 2024 20:59:42 GMT  
		Size: 156.5 MB (156481671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0dc8d622d4b420e561e2d291f36de2c0b4e4b62b85c661b4ec2575d054754`  
		Last Modified: Fri, 06 Sep 2024 20:59:46 GMT  
		Size: 80.7 MB (80698729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4886863837f28f51ab75ba7dd2a7daaec3abfe7bcd045eabbdf6389e4a9d6c63`  
		Last Modified: Fri, 06 Sep 2024 20:59:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c380b8e570bbe0fc3216089c856b5408381a4b71c3b4bf7bb0e1606af22b7752`  
		Last Modified: Fri, 06 Sep 2024 20:59:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:797492cfbbae1eca8bfda50ae9ead2291d5bdf436d3d8f8f95236d84d8db7e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e0e028c75b166a6abd5a9dd781513eb8328a2d658f1f294b7d63b4bf8e9540`

```dockerfile
```

-	Layers:
	-	`sha256:24f4c34bfe17243d9008a595d3eb908b4740ee11c2441dad11ce791257b06045`  
		Last Modified: Fri, 06 Sep 2024 20:59:43 GMT  
		Size: 7.0 MB (7000149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477edc1227563aa10f7f7d82339c9373c312a9e7e1fc75e67ec2cbf856a4ef34`  
		Last Modified: Fri, 06 Sep 2024 20:59:42 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78ade8bc18f9cc8871657bdfeef3ee480e358af2efa7271f34820194ea3fc5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284537654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8062b11818892b04b30b3f86765a906b821eea78327affb75a15a1949475452`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef85e1ae411579c6244e8292bee16b65c142fc57f5e3b6a43444fc8fab9c9f3`  
		Last Modified: Fri, 06 Sep 2024 21:41:11 GMT  
		Size: 154.5 MB (154503717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478bc92b654d348eee56cb616ba1350044d108b86df24f6fde78c5900d6899c9`  
		Last Modified: Fri, 06 Sep 2024 21:46:45 GMT  
		Size: 80.4 MB (80447272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c466c3f9a87740a5d0bce71d6e7e6623108d751afc95715bdb8e27add014fd74`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f785d70ce82ee93757863d12e3daf0a8b45dc4192f648193a22fe269f3bc1f`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:3958b9d624eaf061abeca6222cb75a86cbad69ed8606ebc844451d638a1c2dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4d102bc7b70df5e2e6de5c6ea9df5996e42a648f51762230191b75c83bb388`

```dockerfile
```

-	Layers:
	-	`sha256:c4a7a7a060452e79f86319df93917e5350956876eeaf945915619b1b0fcceb93`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 7.0 MB (7006560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e3bb8fe2a74a4a6da19106fc12288b0feedb253a74dc0af11d54f679838028`  
		Last Modified: Fri, 06 Sep 2024 21:46:43 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
