## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:1f2c342aee3674eeb6f5473fd11b375ad378da333aa14956da75b79e8d56fec9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b37df029033a8df6e90505b4ca768091cc0c1a6b3495bd54da4a22106502a56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178468940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fee8529ce7065d022c7b04dd516e7dd3f597b86f100efade24d6e737ddbe234`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:40:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:49 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6621200eccdfc832b4adc987297325021879f086bd764612a44c87dab0f53d1a`  
		Last Modified: Tue, 17 Feb 2026 21:41:18 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c673b2cba519782a16a5479ea5e778e79e76dc5ddd5022e81452c746f475b9`  
		Last Modified: Tue, 17 Feb 2026 21:41:24 GMT  
		Size: 69.5 MB (69541925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac778b6927d3d655dcaa5e0a9b6860067a594230735d8076a90dadf0973280b8`  
		Last Modified: Tue, 17 Feb 2026 21:41:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b69d959e6478197bef984ed1391f8caf3b1d972f68d0e9b16954d547596c2654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7532901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a25353bb2229cf220181e272ed6bbe2201d0fe66b6a6feeab054db7792750f2`

```dockerfile
```

-	Layers:
	-	`sha256:709aa6a65d6b6c05d4bab791e5ef888d2185fc8185ee65d6511ee964b4481acb`  
		Last Modified: Tue, 17 Feb 2026 21:41:22 GMT  
		Size: 7.5 MB (7518707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c19cdac5f0de2d2a7cfb4300d5cc9216038c7ba783f6014caa53f256d80540`  
		Last Modified: Tue, 17 Feb 2026 21:41:22 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15bbbae606114ef7b3689e27fdc5f2ba34a7d90ea136c00d2c488ceb5aa6d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176203888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609505b07ffab6364f408ad124b3f132a2e5b0bb820fad7113df65ee4b80b174`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:40:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:40:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:40:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edaf87630d10ba0ec217e32d5d54fd6ce370a4c7d5a3985e10b08f5c5b0d46e`  
		Last Modified: Tue, 17 Feb 2026 21:41:11 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718f07d45e3efa17e68f9997dc626b6606c41973e45d6ffaf01a793ff8cf5347`  
		Last Modified: Tue, 17 Feb 2026 21:41:11 GMT  
		Size: 69.7 MB (69693311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b41e202b76c6c3a2532708b1881711f8e5cd4194491cc86eed27e5c49ba5a`  
		Last Modified: Tue, 17 Feb 2026 21:41:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:549890577a6e7684ecbf3d43e5543f8745bb9bd5f2106f648a5fb00fbb41a001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93698b034c4d680039ffcd2c39c3f3e05378492da9dc1cc30ca2b269f7a9bb45`

```dockerfile
```

-	Layers:
	-	`sha256:2bebb50060d764e3551ac244290ca23043691a5d3da7c71709d75cf4e476c9f7`  
		Last Modified: Tue, 17 Feb 2026 21:41:09 GMT  
		Size: 7.5 MB (7524506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd28335c275ca7c24ba204983c651e35cf689b712ca60f416ab22ee50947ded`  
		Last Modified: Tue, 17 Feb 2026 21:41:08 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json
