## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:b980586dcd0a8bae6524557dc4ac14ba7b2107793d3bc00f6e71c862d6bb77be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b2df8f37f5c2cba92ac1d3cd43ba3ad03f915f58071ac0a141acbfbfabb38cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268742441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81381222441e1b77691894f8996b09e569b9db49758278fb2fb3898f5d1bc38`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f794d5fc1c4658df4da6d920bc7b1cae9d39d796f84959bf2bd7a6dab6449c`  
		Last Modified: Wed, 09 Apr 2025 02:18:34 GMT  
		Size: 145.6 MB (145598787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c346bf39b7bb1955fde1ba0e317ef18a6be88077f4e3e3ce0e70b3089b8868f`  
		Last Modified: Wed, 09 Apr 2025 02:18:32 GMT  
		Size: 69.4 MB (69394480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba9195795b0ae5dfb4695bec4950952cbd3bf5bb2aeffa37c6ca568c07bab2e`  
		Last Modified: Wed, 09 Apr 2025 02:18:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:483dee6cafe257015bf5ceb678b61db05cab4c8acea69d6f7c50ecb39f91ddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980a02b99df0ca9b5dab002187e037dac0d5f80013543bfdfdd292261afff5b`

```dockerfile
```

-	Layers:
	-	`sha256:77a5a970ae8a06ff46401bdd00793e367df67d6f782bd8053df875693519a2db`  
		Last Modified: Wed, 09 Apr 2025 02:18:32 GMT  
		Size: 7.2 MB (7226642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba247c907522d8962ef55fad5577ad872f2ae1aaf161dd1c4333731de8b6c227`  
		Last Modified: Wed, 09 Apr 2025 02:18:31 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f547792b28a4614594c7abe84c9ffedd234ad65159a28df5df5601c559a5f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264170036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4af7969989005ebd9ebcd4f92a70bfeff4c8397167ef1c43ea7daf5ec1667`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b2a3c03b51c9a496dfc18f0fdcb0e9ce337005cf1752ee258368c5843340e`  
		Last Modified: Tue, 08 Apr 2025 11:21:12 GMT  
		Size: 142.4 MB (142385472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f25fc35035bb866bb0cba138f66188c297a39f34624d59867bb2e7abfbae67e`  
		Last Modified: Tue, 08 Apr 2025 11:24:08 GMT  
		Size: 69.5 MB (69529696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88455cbd5ce8324c2308a703d857f1c02d3681f08e5a66e306c321eaaa80da79`  
		Last Modified: Tue, 08 Apr 2025 11:24:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b336c44baf69e216dc5556aa18fd1c58b6a6ccdcea14984e58695ec4f8b46a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29087f8d194c12a3a8e5e26204df4be7d5df992415f65d6d983786050c9d4bd6`

```dockerfile
```

-	Layers:
	-	`sha256:6b7d830e4c7745132910a0e2881e1c4ea3dd95da8af2205c78ab534a1272aaff`  
		Last Modified: Tue, 08 Apr 2025 11:24:06 GMT  
		Size: 7.2 MB (7232359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947e8088f6c07a28cff1790c2564654e27ddaf0addd565cf603824da958ae90b`  
		Last Modified: Tue, 08 Apr 2025 11:24:06 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
