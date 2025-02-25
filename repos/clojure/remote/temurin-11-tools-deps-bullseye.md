## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:15c77cbe380b29dc23d87d1207c0055baadc475333c41a97a067808f8950ab53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:964e85bc5af2e0346aeecc23185992ced8666625156a47b137a42abb0efa03f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268528455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07719ab13a77467615d19a5194841ce671ca3eae12611e7f8d5431807d9a791`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e3afbf72c7a632600939f6f9db7cbb1bfe7dc59754f1e0a9df3386b467661`  
		Last Modified: Tue, 25 Feb 2025 03:22:15 GMT  
		Size: 145.6 MB (145598925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ee1cf8eca8f5e0bbfd6be112d1afe0e32bbb325c5e7f7c8102531ee8e84e2`  
		Last Modified: Tue, 25 Feb 2025 03:22:14 GMT  
		Size: 69.2 MB (69187483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8554e98b3a571ef402545d7ff5688fa52690176fb13508891b72f49f0109f`  
		Last Modified: Tue, 25 Feb 2025 03:22:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28de86ba424f991a49a0942eacaf0bf9d39aa2be33ac8075f9c293a89fa40303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d068fc98c109ec84cad84c907c0be1a19db36a3db1d0ef2e253ea06a3e7d1a36`

```dockerfile
```

-	Layers:
	-	`sha256:391249d8e672a3db0a7814663675374f4d60d106b6f47a7fe4f4574f8e287a14`  
		Last Modified: Tue, 25 Feb 2025 03:22:13 GMT  
		Size: 7.2 MB (7224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b4e0c63bda0cb23f6d5fccfca66cfabf7f83c2e8b3ae8b41d54e50a3bb6fbc`  
		Last Modified: Tue, 25 Feb 2025 03:22:13 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

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
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b84d856a8cda7ccd0051435c1ec5c69d9363b1536c4989a13571127e1a59f2`  
		Last Modified: Tue, 04 Feb 2025 23:35:23 GMT  
		Size: 142.4 MB (142385421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3bb6cc76d4b086c7aa6276d84f2f054dbc61e4d6352ce04c54cf822b222ba0`  
		Last Modified: Thu, 20 Feb 2025 03:47:38 GMT  
		Size: 69.3 MB (69309116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8347fe92e7217e2176f5f36b323954c47d95f04a786b3947a35acd62a24fb256`  
		Last Modified: Thu, 20 Feb 2025 03:47:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

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
		Last Modified: Thu, 20 Feb 2025 03:47:36 GMT  
		Size: 7.2 MB (7230413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df888d3309354ab63863d2289375d032b6815ef702898e7c978c85df408f867e`  
		Last Modified: Thu, 20 Feb 2025 03:47:35 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
