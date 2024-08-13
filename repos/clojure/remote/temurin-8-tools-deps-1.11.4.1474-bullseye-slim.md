## `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim`

```console
$ docker pull clojure@sha256:644f56734652599ec603ba5d75b20297b884380528fc853ced8f953f6bdc944f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4daaba6f5503cc2a03a70dac26a12f8cdef6ea6a0db4f3184c4e13b7a17e1cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e457022c8ddf00239e534ccff37a3ee494c131b956287af1403a61b9643441`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d654a11e68d8354c0ae7c6586268ac5a7b2175307b82121c8799a164107165`  
		Last Modified: Tue, 13 Aug 2024 01:11:11 GMT  
		Size: 103.6 MB (103611906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7b961e4a5d2f7fea28db2ca18b8c2405e204380df0371561b2ec83a2b026fa`  
		Last Modified: Tue, 13 Aug 2024 01:11:10 GMT  
		Size: 58.6 MB (58572010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eecb0346e0ecb47584c1e8d3679c17840cf90e85af745115a3ffb74262ecc51`  
		Last Modified: Tue, 13 Aug 2024 01:11:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5db662115ddaa0eb634df51c21418670247db6a86caba426b0378e66aef3942a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4989237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370df87d8f84eafd3f1ad1e3aa82e28cf1d56e5c8083ed540d7ed44c0e0d3579`

```dockerfile
```

-	Layers:
	-	`sha256:3b91132bb56a83187c3da48b64301b2b856cf5f5ff794cc7d79ac703042c9b38`  
		Last Modified: Tue, 13 Aug 2024 01:11:10 GMT  
		Size: 5.0 MB (4975317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121df541cb24d3bfedd268d5f6dc1b53dbea3f10474c216ce2705c35af7e8e72`  
		Last Modified: Tue, 13 Aug 2024 01:11:10 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ec1d099137a420635de981e899fd242ab02e6069b1896f3bcf6d3cfa73dfc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4a5e9754910bc6a5499679c093e67f4fea74ec26c362589b6d9b642075135`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0813be99e5fef18309cedf80ba934aa71a9e9724621b1626f3edd869359e2519`  
		Last Modified: Thu, 25 Jul 2024 19:10:40 GMT  
		Size: 102.7 MB (102729198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84591579725718c587fd97d5b7e4574fd14a33444778af8fbf9a03a1dc434899`  
		Last Modified: Wed, 07 Aug 2024 19:45:26 GMT  
		Size: 58.7 MB (58699682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8610976ccbb6f50d1bcd3fba02f293d97dacffe2d55f11a14f30f451555266`  
		Last Modified: Wed, 07 Aug 2024 19:45:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8147b0b66102f01ee234b3fb73ccfb3d874fc75b7bf32c8967b634b0434ebe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b3c5ecd61716f4724ff3d0fcee12443ffb220c8c0484d70dfa4726497e065f`

```dockerfile
```

-	Layers:
	-	`sha256:f13e3f38fb333b112dcb0ab5f503bdcb7b5d93bab9f2d3b8637023322b23f1b0`  
		Last Modified: Wed, 07 Aug 2024 19:45:24 GMT  
		Size: 5.0 MB (4981673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc4638e9f64a58f36f548b3517310df314de5f52a0626975aef40145b3dd93c5`  
		Last Modified: Wed, 07 Aug 2024 19:45:24 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
