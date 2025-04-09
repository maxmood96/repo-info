## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:4ec63a27d902f3f7f6063515495c8d2d05a0e3cdb97585665e3f8033d2118bc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9af583cdab63913cac69504a94dd89fca419998e58dbe7cba6763bc93964910d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233817792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cb9107b689036fc84189589b15352da13bca42cb19b319828bdcad831b95c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0238cdd747238aa54036a3e440a7f27a7d74dcd00708f33eafecb324cd0ea92c`  
		Last Modified: Wed, 09 Apr 2025 02:20:03 GMT  
		Size: 144.6 MB (144566536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cbf2ae43aed20391a9ae77fc72b3a19aed0a581c6d23aec7c3020d34bd394c`  
		Last Modified: Wed, 09 Apr 2025 02:20:01 GMT  
		Size: 59.0 MB (58992793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b16ba2fe3f7968998fe3851d1bb6e760914d82efd73c925d188bef51e54458c`  
		Last Modified: Wed, 09 Apr 2025 02:19:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8bb15013f461bb80f18fe41ed3d9603f3e7e4064cab133d60c1f02886f3b7`  
		Last Modified: Wed, 09 Apr 2025 02:19:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd6daf7f32f989321f717b79fc01add3235e9a667ea907d8ee623f447b429eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25728a1e8a51a701686effad4a8f14979aea86bfd1c6df67158e9193e7b9c499`

```dockerfile
```

-	Layers:
	-	`sha256:67e2948e657afb19cf34c5dd5183a15c08785029bd1e31e4d6da87bac904b255`  
		Last Modified: Wed, 09 Apr 2025 02:20:00 GMT  
		Size: 5.1 MB (5119013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c0302bf71e66e2a4ea47b638a56f1fa36f4db7422d8105060ce6bb3acb44d5`  
		Last Modified: Wed, 09 Apr 2025 02:20:00 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d23041aba3d5358465a1fa8a72e7b7c832f3427942ba2c6a9c218a8acf52861e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231332123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ef38350a0467ffe827b7bbf16bd5e2cb7234f0ed74caa89ccd5e68885d3dfb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc61d01d3c1907bedb7211a2ec04da2c97e8407d17c661dbb3fccaf3036cfc`  
		Last Modified: Wed, 09 Apr 2025 15:18:21 GMT  
		Size: 143.5 MB (143454624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ba804dce129e7fc945504333792e6bee33983ecf9e5a18b664c0eb957d70b0`  
		Last Modified: Wed, 09 Apr 2025 17:36:36 GMT  
		Size: 59.1 MB (59126959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1acd4f84a90f5b3659d0db10345228dc6e36dbb00fd4e16f9836be2f24e188`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f87153d3dd33cfdf36462acc499f501dd0baf452bdabf0ccfd185f1c5e28e0`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a0a0b95e746297d2128da3630af359be8b2697b89d047009b165d8985de3051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1ff3f72b62615549d0d7c543417dfd95234f3674b94ff9fed7a633d6174392`

```dockerfile
```

-	Layers:
	-	`sha256:87ba6034729a459df29cdce31d741985ee87ad8d3a094d0c8584a971f1e10d69`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 5.1 MB (5124745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4722736cc92a92540b34e6df44c8ca6bdd18ba719eb6122764084fccfff54d3e`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
