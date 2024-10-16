## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e5b1c8a59628ebb4aa6b83f5b92066b0a2f32545df11aa832f57293607c0b003
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d72bfae989ae42534dbe8203da4fe5ecda023c887fb9c54e2d762902c74260e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c463498c099c0c242f2f373bb760f1a5e462765d3f8f14826015e7c6ebae2d`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070fb27b06add8af90f91be0831d34a86ae7526d00684e620f34db9eb5e1466a`  
		Last Modified: Wed, 16 Oct 2024 16:12:59 GMT  
		Size: 145.5 MB (145549907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcb4f879ddac71aedad9cfc0ed041b8a42ca8a2c00464255eef2fe70802eeb`  
		Last Modified: Wed, 16 Oct 2024 16:12:59 GMT  
		Size: 58.9 MB (58939998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358ad328be739fddd08796442ea84bd0f235383c7eed557a920b3fd4184f90b6`  
		Last Modified: Wed, 16 Oct 2024 16:12:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5799e814a11e2ce4c6413d94b754c36b3e0b5dd8fcab39b20baee2d52fcbefc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54228aa77e88200c010a851b4ddba7c09fc2982cc9bed1a79684a5c44fceb18d`

```dockerfile
```

-	Layers:
	-	`sha256:8d9d5024b0ae18ca9dde5cb93368f34762339a0b448afe6fe67a2cc7d366be04`  
		Last Modified: Wed, 16 Oct 2024 16:12:57 GMT  
		Size: 5.1 MB (5119652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144f3632323711c1b72a9abe9093bc23b99aa9367fbd07dfcec2a60eb5d4601c`  
		Last Modified: Wed, 16 Oct 2024 16:12:57 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:41b9d5f4b9ec95e62f1a0be1ed3e4a1d720bce9008535760c91fd2f2b5df8284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231505738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911bf25fd4e18e42e6d53124482e85b9229675f26282b95cda986f9ac7b253a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1194c66fef25f7dc81a3ea58a1387706afcbee95076b271eb17e9ad408f2d48`  
		Last Modified: Wed, 16 Oct 2024 02:14:37 GMT  
		Size: 142.4 MB (142356565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fbf597873473a5dd2b81d56738fa629b6befd8490aafbf8a5e155de77fde9c`  
		Last Modified: Wed, 16 Oct 2024 02:19:07 GMT  
		Size: 59.1 MB (59073369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a5a2e9637c92ef049463938ea9ab4e75275af9550d5b3c7820e2d4acadac50`  
		Last Modified: Wed, 16 Oct 2024 02:19:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e43594b1b039577efeb77293120b57a2cfa8d7236f3e3c626106cff83836ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad91fac1ab1879b1878aea50e7928c53e71f7b9e45ed856827296959e99c54`

```dockerfile
```

-	Layers:
	-	`sha256:f74d7d919bb986fe0cbedd6913e0b907974314bba1567c710c696c5c23fa80c9`  
		Last Modified: Wed, 16 Oct 2024 02:19:06 GMT  
		Size: 5.1 MB (5126008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7412a363571deee255ce6f3fd33dbfaca5a318fae7cbef47c15f9ca49446c8f2`  
		Last Modified: Wed, 16 Oct 2024 02:19:05 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json
