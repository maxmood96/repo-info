## `clojure:temurin-11-tools-deps-1.12.0.1517-bullseye`

```console
$ docker pull clojure@sha256:bdaba74ba9bcedbe8de0ab7c79cd56a9277c5c8c86fce45e24d362a605b2e1c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1517-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a27af2f604b1b0d03b9eede1fed7b5d944bb3889b877245d3b0264a8a66e83e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268525893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d9e2e723c763460508bcd027c54b049b60a1b407df9b0bdc8c1c278ca77b2d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c367893c9db31ed48978fc38a7aa6efea0d892bb4a1db313562389faafc973a5`  
		Last Modified: Thu, 20 Feb 2025 04:11:25 GMT  
		Size: 145.6 MB (145598925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2646e7dfe8709c89095e177e77db516321acf55fca0ae3cbc9c83f9d07c51a7f`  
		Last Modified: Thu, 20 Feb 2025 04:11:22 GMT  
		Size: 69.2 MB (69187453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f0e8b4c1f53f014efd72a20f975045191ec2c61bad2558e260c235729aed4`  
		Last Modified: Thu, 20 Feb 2025 04:11:12 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1517-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b00ad3bd97f395f9ae21bc4fa11b51e9cef9e6a6bef1952f4076bb484d8e34a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e95a21fb0ec52129984c8f907662b02dcfe2dd4a3b339082207d9afb658c7f`

```dockerfile
```

-	Layers:
	-	`sha256:59a86e03467b4355851d3a23867bf4c8c08608c2afddbc9975fec180016d02b8`  
		Last Modified: Thu, 20 Feb 2025 07:34:24 GMT  
		Size: 7.2 MB (7224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72ca1ef425115369b779a86443a16d51b6edd4cb0757be6690ae00a0b70c66d`  
		Last Modified: Thu, 20 Feb 2025 07:34:24 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1517-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b5420d9af35bc94aa82b34c3e8cc4dfdaad42a58881c74e8916e62466c8a1fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263940877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b208c25a71cdfa32829c7aa138cd881d8b3cb6b7d0a95c7a900bd76e825baa61`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 04:34:59 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b84d856a8cda7ccd0051435c1ec5c69d9363b1536c4989a13571127e1a59f2`  
		Last Modified: Fri, 07 Feb 2025 08:57:44 GMT  
		Size: 142.4 MB (142385421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3bb6cc76d4b086c7aa6276d84f2f054dbc61e4d6352ce04c54cf822b222ba0`  
		Last Modified: Thu, 20 Feb 2025 03:47:48 GMT  
		Size: 69.3 MB (69309116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8347fe92e7217e2176f5f36b323954c47d95f04a786b3947a35acd62a24fb256`  
		Last Modified: Thu, 20 Feb 2025 03:47:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1517-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3ac1c08d22c8dfa9001ef9065ca9beeeee3bad79a41e0089af2daf975e5432c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576714c18d8afef5094c261b8bdc52bf50451a6c1c26c482f53628da9886608e`

```dockerfile
```

-	Layers:
	-	`sha256:4fa2bef5a56363f707aea44b790f746ec0796d89a21cf151423f2a1d851786f3`  
		Last Modified: Thu, 20 Feb 2025 04:34:52 GMT  
		Size: 7.2 MB (7230413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df888d3309354ab63863d2289375d032b6815ef702898e7c978c85df408f867e`  
		Last Modified: Thu, 20 Feb 2025 04:34:52 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
