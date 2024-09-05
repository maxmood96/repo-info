## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:84bb2ca76b174f4e2a3677538479e53a5301e3be11ef4610c8cf87d0b315d52b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc94f9274707aa5e27c6ca606df8767ea8e5150a5b97718137b324c4a808a59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240285566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1261702b555f3d46eee6daad8efd754c1eca492cd7916d3e824931b3d6be2ece`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21e04edf6f0707618ded0c1ff6a94764c25f714abaa1345780da846e579ad9`  
		Last Modified: Sat, 17 Aug 2024 06:02:09 GMT  
		Size: 142.4 MB (142354842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6888a740268a23e9bb9e462e39e88072c3242140f52c4da4731f2deec924d374`  
		Last Modified: Sat, 17 Aug 2024 06:07:22 GMT  
		Size: 68.8 MB (68773549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da65e64ec6c524b6dc2a6d89920c57da5e213e23a1434cfce7070d8e1c6a157e`  
		Last Modified: Sat, 17 Aug 2024 06:07:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af17a6f7268f83a48246dde697d6f6467e02c1ba64593bb2d8aa6777f234cc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ab2847456f0c333a3b74a548fb54c0a9985355d7505e33fb8a1a3e4dfb82bb`

```dockerfile
```

-	Layers:
	-	`sha256:918b568087afeb0aaf0c7ef69e2d2de802929e44d8c83158044e5eba59fa2a3d`  
		Last Modified: Fri, 23 Aug 2024 23:54:41 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1106309c04056b4ef0a1835ec36ec517f1e1427fe940dfd8ce56edc4861014`  
		Last Modified: Fri, 23 Aug 2024 23:54:41 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
