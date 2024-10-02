## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:ca4d75a6749b9a9d023ff6932c06c4af7ba80374486adf33f959eef6a8bb0409
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:421e83e2d4a228eb16612130db0ca909f3b84991410c2f1bb293370e2f8c4b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269582629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963d72680d7c95c4a4942070558adc37f486ae45501ae42b594392590f5d823f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd129c7394ed56dbf5c09b3f53e446057f0e5a84f968849d0f3a0d91a5487244`  
		Last Modified: Wed, 02 Oct 2024 02:57:47 GMT  
		Size: 145.2 MB (145166550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a0ce5de59f3fb87189ac6155e4c738c31b929f76f2e7b2ed37f72172899afc`  
		Last Modified: Wed, 02 Oct 2024 02:57:45 GMT  
		Size: 69.3 MB (69333648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719c7b6dba5369fdb4dd697448ce7dde009ff5fb093420ff237b8bf44e33c398`  
		Last Modified: Wed, 02 Oct 2024 02:57:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9966f3e881fc1ff2a6444aea349370d3ebcad82bf5e610f52b28cdaa9b7e666e`  
		Last Modified: Wed, 02 Oct 2024 02:57:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01418961a8c14fc53c08ba905ef7bc856201255a9c4e8c7eab42ab6a89cca5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a2371ca575d285668b9459ed130f49c5c3a746dd12f7a29430d3e42a35ff64`

```dockerfile
```

-	Layers:
	-	`sha256:d25bf94bf0ccd0814bc79fb7abe92c871eebbdbde2156f3b921c395abcf49c01`  
		Last Modified: Wed, 02 Oct 2024 02:57:45 GMT  
		Size: 7.2 MB (7189363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acba2f389c47c160f6f97fb57f60b56fdaf0591dabc4383014b8a7f5e784ff17`  
		Last Modified: Wed, 02 Oct 2024 02:57:44 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cb0790d17df0e559fc932961b03295a0d781f29994e88a42099fcb186b3727b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267161256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aa68975d35627296dc6b7008b8747a18c12785c4c1ee42a77601d0c754bcb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8e53f51115cb1617ad945c8fc2d38ce44bb07ac3989b7f894bed674c81a4ee`  
		Last Modified: Wed, 02 Oct 2024 02:20:32 GMT  
		Size: 144.0 MB (143959484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b474b04e4b3c72cf50218340666d971a9595ba62dc668cc53de90a4f11ecf3`  
		Last Modified: Wed, 02 Oct 2024 02:23:50 GMT  
		Size: 69.5 MB (69466871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea271f97c6b9e8e0bba3709f6c06bde7c3b8c9938e769e335009f786204c7f4c`  
		Last Modified: Wed, 02 Oct 2024 02:23:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd011afd62b439d7050004b4137b1bf88460ccf0c569e9258de1ffdb12ef77`  
		Last Modified: Wed, 02 Oct 2024 02:23:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:333f78de533ca16d23288d029529600269d62c053d64105ddb8c12fa8fee0770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5243984840036c80171a5e4cc9149e72e5c1295712dc806c86f8db9ef9033599`

```dockerfile
```

-	Layers:
	-	`sha256:87baada64d6a9564168391589108f21636614b906204bc58982413589f465aa8`  
		Last Modified: Wed, 02 Oct 2024 02:23:48 GMT  
		Size: 7.2 MB (7194466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8370adcf35aea5626aa40225d1025ef25ffc3050643c1a9e2528ec99304140a`  
		Last Modified: Wed, 02 Oct 2024 02:23:47 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json
