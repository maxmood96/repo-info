## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:941f1b6f2ce4b2d6f69c4f408d7324a3e08e00a299f92aaff7568804e25bf541
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:854bcef83565abd34bda74790ef4047bcb16a479d0e30c88d10dc0848fc5be85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263905236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba87ec14f673cee1ccf0fd9d693288a3b6ce0f34784256ce002f427110df28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10374043d595d65e137c7906dac6363fb6c87450a63126c0f58d2e366449dfe`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afac3f656c27fe35b45c5325d9ebf93e6aa6b969f62ced73ce49db871c95e604`  
		Last Modified: Thu, 24 Oct 2024 01:56:51 GMT  
		Size: 69.5 MB (69482770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0bf437f0660eda22ec6e1916198809602f3bc65f82fd8f13ff67f4af494eab`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e46453577d0cb01426ab5072cdb93af0add562ba3e13543e9a2e1dda3f7e15`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:be6741eb32cd193dad5614bfc35683d0ed03626aa37317082b1d9a07386b0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0211eed5a2e5067d7a1a4ed43e83145b9e24f323f0f078823d5cb84134c840d7`

```dockerfile
```

-	Layers:
	-	`sha256:b600c756fe24c9646b389ed15f8521d5d98ee298a69bc5c85fcc8a108cd1da05`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 4.9 MB (4925605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f5c02560bc42f5bc560db9248074c0f72dfd13beeb20f6b5ce1c4dfddfe3da`  
		Last Modified: Thu, 24 Oct 2024 01:56:50 GMT  
		Size: 15.7 KB (15682 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70230f19584ac873ec490b165791b20961a199f7dcd750e2c09f2b063bd67022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261755300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c4eb44dba8faa4b36e2a25a8e1d385692501a9475e6e5e1db6c13442e624e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7943d41d804563f03bfbce62b1be7dded9a88ddd348486736a41f14fb75c989`  
		Last Modified: Thu, 17 Oct 2024 08:28:47 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e7dc8e4cee0156078036fa6468f138f75ab3bbfddf5b98156280e4abbc90b2`  
		Last Modified: Thu, 17 Oct 2024 08:33:24 GMT  
		Size: 69.3 MB (69345119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283773d967eae6c70a240cecf0d0b6521f922cb9c533e96ef79d9367539cfedd`  
		Last Modified: Thu, 17 Oct 2024 08:33:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3361b0a2d491ec394063f36c727d863353807703307ea2a1ea60cf09d4c2e701`  
		Last Modified: Thu, 17 Oct 2024 08:33:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9cabdbfff4f1753101997e9d1bf19d9228164b2815d6ced21459f640e2c1aa54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857e08986e5943232d08f9d783e9506e5fc3ee78a8b4bb3294b7de40a250d3d2`

```dockerfile
```

-	Layers:
	-	`sha256:1676404ccc38e51d99bcfc585f81bfc58da446253c05650961d23d793123934e`  
		Last Modified: Sat, 19 Oct 2024 12:22:40 GMT  
		Size: 4.9 MB (4930733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b921974ee84c6f4cc4f90cbb8ad050c654a7fe980bcae68ae8bb9611c74b38`  
		Last Modified: Sat, 19 Oct 2024 12:22:39 GMT  
		Size: 15.8 KB (15830 bytes)  
		MIME: application/vnd.in-toto+json
