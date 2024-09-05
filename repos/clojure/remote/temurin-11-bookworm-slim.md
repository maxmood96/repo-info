## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:c4dd1452a7e4ced3f6e1aaf69ee0483e514bda848decbc6812eb4dd4aa1bd9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:84a39a5dafcc1ebb02174acc40b384cacb49f38b17338f778e3f70057245ee3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243704823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb005dc29cd850298adf6453c2dd47524675fee60c00d1584a2c3a8c1c4bb0a3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a358323220982cb390592e4fd944bfa7055077208cfb4f00154ff345c54f9e8`  
		Last Modified: Wed, 04 Sep 2024 23:07:47 GMT  
		Size: 145.6 MB (145550052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9609cb928c846d07b97813022b10fe95d709b44d2d37bbd9e25b358906e03320`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 69.0 MB (69027640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f9391ecd928733478878510f3ef4d5bd9e7c311c34e69904dd53dd421bed2d`  
		Last Modified: Wed, 04 Sep 2024 23:07:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1df6318933245f1b56756628a83e641abd2035ffd31647d417867efce8f0bfe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26061dfa434e6a6780fa0fbba7ec6ec0284d93d9b8b6bf394eba27dab87bf1c`

```dockerfile
```

-	Layers:
	-	`sha256:13224b323315c33f54836f8b6ed97db60f2714f2fca59f041cb19561973bef74`  
		Last Modified: Wed, 04 Sep 2024 23:07:45 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec4fd0dedb00592e517d7e71bd2e62f640fe48d79c51fbabde0a3a4125b03e2`  
		Last Modified: Wed, 04 Sep 2024 23:07:45 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f3ce7c7716d3413c5fcce77b079e58db36f94c17840231c087dc98028c6e334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240285341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0456debd9d2844c2c2fec1ceb324cfcf5c9150dbced701d45297bae1cdf7da6d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
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
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2957fda4b001cfa06e2d0a0cc9897929ab8cb72408369b18f74a60f55e8340`  
		Last Modified: Thu, 05 Sep 2024 07:55:50 GMT  
		Size: 142.4 MB (142354898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d5a8383d81e0d1ce38df28f3e8e26445e0961ababd8d6d14ed3f63ef984476`  
		Last Modified: Thu, 05 Sep 2024 07:59:19 GMT  
		Size: 68.8 MB (68773250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea70711f19258ed565f8f3a10f48ed5c65ce637fc9a201e481b03c84f0bb8a42`  
		Last Modified: Thu, 05 Sep 2024 07:59:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b0a033b6964a7bc759534179e303a54a8205f940a062365c737e376d69582a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecf9009a4d11d803533a02cc6d0a35d4dcef3cba02df8b264443c8435c0134c`

```dockerfile
```

-	Layers:
	-	`sha256:8414ce39c8c1ce32b4264ccded73bfcd1e5dff185480e7278afe917ae1b47718`  
		Last Modified: Thu, 05 Sep 2024 07:59:17 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55ea1e6c977448ddb71c74a257e642ded0e8cbd37616f572376a2f35bccdda6f`  
		Last Modified: Thu, 05 Sep 2024 07:59:17 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
