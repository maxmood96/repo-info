## `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim`

```console
$ docker pull clojure@sha256:e50c328379fe7a941cbcbe146e32501e5c16457c715682aa64d8e114e1830e06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e12cf8ab9fac0ad41835b56eac435b703eeb9ac56797da02c612b8a2cfbf1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235298520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74825b63f46159e8de117959a948c4ad24b9ecc975f88420cec10fdaba17e18e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abd4e4463045cd8d9e38d751d77499d5b9d3f7fe013d553db0b633d99394cdc`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 145.2 MB (145166561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb5fe4f0e86312711c3ec78d308c32c6c7068ebc60e32d573faa39146a573a6`  
		Last Modified: Wed, 04 Sep 2024 23:07:50 GMT  
		Size: 58.7 MB (58702241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6874a894602a521f449a7a49043f810a2e6f33479cc1df2f8cc1f3240945cbc0`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf4244edb971f9db84f0fe119d1832f4cbdb9bb4f25b87a3363b4c07a018699`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c575f9ae90b69eeee01eb73a19a318452f89c507d4635395dc909bf0098e244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd84111e6256f6b8e83b27f237e67368403e95eb137b062341651882d342700`

```dockerfile
```

-	Layers:
	-	`sha256:ba9c63fa63a8a055a91c57546c9e83119bf0ab5513a2661c2ccd058b6fd6b8ca`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a50991803026e0aa7050c061ebb65d23fbb3d503a2b049fe449f4c8bcecebf`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94f0e469c93eca938abf6ad9ba421e0baf3f175bfc33f2a22a991ed9aa94e80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232736094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ced618055379bf5db1bfc0dff54758b822871325e746abde958b5924cc3f35b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98da5f01240526716f41e0ea14ba7c0ea210096453b2a7950576dc4acad8096f`  
		Last Modified: Sat, 24 Aug 2024 00:00:57 GMT  
		Size: 144.0 MB (143959469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f917820349d256fe392b32f53006df75c2ff5aa4786fb41fbd2477213d84d5`  
		Last Modified: Sat, 24 Aug 2024 00:03:56 GMT  
		Size: 58.7 MB (58699494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3114beca982e5301fc63189617030b311513bf8bc643ee92840e9d36cd73c3`  
		Last Modified: Sat, 24 Aug 2024 00:03:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1d3315306295ec4512f81d9e7f53000c55adee4b3bb8904732351feed78953`  
		Last Modified: Sat, 24 Aug 2024 00:03:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f933826f9ffb31cff44b6917f18c11e338f37cfd2201470bc3477fe2cd03f276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f9a8b640d9a40512d4d9cb0c88b2d3ed6d801b0865344e10031b5fcf3b1366`

```dockerfile
```

-	Layers:
	-	`sha256:5ddcd173e1e231dfa80406bfc59f4d1f2c33ed98194e75560c2fcdab8b227cc7`  
		Last Modified: Sat, 24 Aug 2024 00:03:54 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd12df69036b8b5579ffbe096373d4a8ed6a85015db83b80c93fe731c6c54c9`  
		Last Modified: Sat, 24 Aug 2024 00:03:54 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
