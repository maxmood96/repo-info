## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:29980f29b0004881d70309edea90b15e51b09cc58836b558198f205c8174cd5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a8f738dcbad32ea42ee531d14192bb0f5e6b6b15cdeec8ad2413f346540fc86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235024199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a92c5282a620f9c7a834f255c4bb9d177bba129a70f365427fb1a20ee33553`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:04:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:49 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8dd1a47f922076627183600beab551d3d5d4c8750caa36e44c91d33a80d58`  
		Last Modified: Thu, 05 Feb 2026 23:05:24 GMT  
		Size: 145.6 MB (145628407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8ad234af0e66198c284d1b49d771fe694eb66d71f5c0fe1a1df7b5c9c6735`  
		Last Modified: Thu, 05 Feb 2026 23:05:22 GMT  
		Size: 59.1 MB (59136466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1703895695014bd6c4d1ec038cc259e3e93d7a4dce6c1c4b872d53a949650837`  
		Last Modified: Thu, 05 Feb 2026 23:05:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7df85108dc7959946196c95b254adaf09b6332e4c5502eb68857f982e2fac8`  
		Last Modified: Thu, 05 Feb 2026 23:05:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d7aa4e489182bcaf21a597620f1937724a7c8be19230d3d8999756f9308551f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5325956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62ebbd0f5f929d3a94b5356bbc23c55cf269151796ec1cc7363666ec31cbadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2540c88762619221af4976263a85278131f9a5befbde04a5d230167d5c3e44e`  
		Last Modified: Thu, 05 Feb 2026 23:05:20 GMT  
		Size: 5.3 MB (5310120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88a12b7c17914e1a512bb60ab9a51d2a5bdafc7999c482829fa780121d09a7a`  
		Last Modified: Thu, 05 Feb 2026 23:05:19 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93e87286f13c7cf239609587621e55f5ad8bd594bbe8dc596fe5126637f0f444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232469747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6703444ebabfbdcd23a0b6b01d8cc400fc6a5a44cdbf31eea3088860c6548f50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:05:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:05:52 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b6abe686deaa1e3cf94bafa875f0a5e50c665f33e1dde688f693c673938b2`  
		Last Modified: Thu, 05 Feb 2026 23:06:28 GMT  
		Size: 144.4 MB (144436240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652c88de36227e9e4f85593615d68e0caf319198f1f6db0bb98a8d1470f91dea`  
		Last Modified: Thu, 05 Feb 2026 23:06:27 GMT  
		Size: 59.3 MB (59288027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f675d4c5280f7a38e124798562b5db11672e18c782d7788ed224e59f5ae85f23`  
		Last Modified: Thu, 05 Feb 2026 23:06:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94811c0154c3572aa3384b12e61b27c53ff06f15c9d67bfa6c627a7529fd392f`  
		Last Modified: Thu, 05 Feb 2026 23:06:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de25353e3c46a176f5805fcc279a74ee76d04aa531bf35751bdcafc7f7cce536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2720321affa9214c9c1fa5f74f0c1ed4bb44f9a9adf8841c713ca717e26d885d`

```dockerfile
```

-	Layers:
	-	`sha256:0c2dba174b6df58da15a7a8d485da0b596be9583607d01d216cb2e4824aa2278`  
		Last Modified: Thu, 05 Feb 2026 23:06:25 GMT  
		Size: 5.3 MB (5315852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1b80d3ca81be691ce64604657b7d585d817ece5d8e1ea4d310401eef905a05`  
		Last Modified: Thu, 05 Feb 2026 23:06:24 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
