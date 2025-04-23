## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:b8996029937777e5174900573ac7f7ef13ae68c4b1728283da14379c30970828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a70f1968b7d532fd3e6cf6ef43564da0ff20030542d8a9e1a3bf6696d8b3a95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267779787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359592ca705f64acd7f8e2d0e518731456c1c99b8efb8abf96d913081982c40a`
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34ddb9c1128fb8110b6e0480f3174030e12d20587ea0bea3414e6a32098f2f5`  
		Last Modified: Wed, 23 Apr 2025 17:16:11 GMT  
		Size: 144.6 MB (144635006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352c032a7077b7d72da3fe98862b49b425407fe84b1f948d23f6b51f1b10b5ae`  
		Last Modified: Wed, 23 Apr 2025 17:16:09 GMT  
		Size: 69.4 MB (69395205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd91f104449adc53568b8fb7eb4f14157d06a0e35d20f011a3fed5b3da1bfef`  
		Last Modified: Wed, 23 Apr 2025 17:16:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4c0db71df090c97f3f67974ebb0b45d05bade8dcb8cefb3992309b01b66f0f`  
		Last Modified: Wed, 23 Apr 2025 17:16:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3ad84116d80659a36fabe4b073d42ead55618d7774024919ba5a8a0e4bbf25a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12940e983334e7cc55e5911712f7a77b48f69db4a3283d215b08986c2753228`

```dockerfile
```

-	Layers:
	-	`sha256:71fa6f289be394cdb9cf462d7156fd4b5c5ac4a15f8815d6c1dec8268f0cfb8d`  
		Last Modified: Wed, 23 Apr 2025 17:16:08 GMT  
		Size: 7.2 MB (7206501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854896f59271de13de136ea1a9b0f4545f7ff7761a837290321323eb962db0ab`  
		Last Modified: Wed, 23 Apr 2025 17:16:07 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65daf6af311d69e80daf6f2fe7e287721510cef7959e94ec675a9a931a039299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265297339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2940cfb5eba07866d38799119f3f7f07f0555134e034e49824f3d97bcf2182b0`
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a2ebf9d993ea072551f562bc3f4c69216a524aaafb63aed8b85eba29ec258`  
		Last Modified: Wed, 23 Apr 2025 19:47:04 GMT  
		Size: 143.5 MB (143512678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def098b222c26ed0a1d7dc15946f9a177bb894b71de873c3086adca55d797cf6`  
		Last Modified: Wed, 23 Apr 2025 19:51:30 GMT  
		Size: 69.5 MB (69529394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e486f8a3b96efc30eaf724ec576db92b711dfb15323f7ab2835ba0f63c3ce6f`  
		Last Modified: Wed, 23 Apr 2025 19:51:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dc0812b64417f58d84bc7fe7acdcffce0f5af5503aaa2d0edf9528c4e08c82`  
		Last Modified: Wed, 23 Apr 2025 19:51:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2dd39311835437f681fc1fd1a4735d7e92f0b6241addf6e7649e7fd3754f7a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a0996bb0ffa777e88a52c90dc9e947df5d1032371bb2bcb85279a2ba8a2557`

```dockerfile
```

-	Layers:
	-	`sha256:a71a1e091c34f3f0403bdb8bcf4558afe957178d4edea07645fa436748def4c9`  
		Last Modified: Wed, 23 Apr 2025 19:51:28 GMT  
		Size: 7.2 MB (7211600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d4318afb8c48c45acdfb31da106c6e15fb94a863f565e22bc0a682642bcea`  
		Last Modified: Wed, 23 Apr 2025 19:51:27 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
