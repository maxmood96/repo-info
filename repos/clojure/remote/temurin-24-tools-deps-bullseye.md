## `clojure:temurin-24-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f2caf3ad568acad1e9b3eec431d48f99e43f3227d882abf97ee09542b294c013
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6fca8dff854596397e995e5aeffa7c8d26b7dee25670aea9da7918df8d626800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213096821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4287c6673d715cc1afe8ec63e207f53a41f31f123fbcaca566d6fa4e310309b9`
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
	-	`sha256:dee42e78fd78442427d7b1fd5874548153b4147c3bb4c0620b7fffe6d9992563`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 90.0 MB (89951972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b00e61a7ba01792e529194b9f0ebe0c0a81a2c6888643a971ceea6938bcb90`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 69.4 MB (69395276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c7f96cf7a88c1d64186418d6fdf46d57207b47bb683c7a5160eb0d9431aba6`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38490e4e176f32735fa4b4b88c03eaba3164af2caa5fa7a7aa10e2cd92648c4a`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1b0504298a8d33b9d3ffcb7e5192f842f64a34f8ced702776addefec845471ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f06b1d8957fba2b23e2ac59f4faa37a7956bf38933051f0705e3faa7251a53`

```dockerfile
```

-	Layers:
	-	`sha256:0d3d00374870c1dfa411bd486a000a905f2a6881c435683a5f5166957ea07bdb`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 7.2 MB (7157147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e73cda32f7939a73b8e8108f989b45206d263378b46f9d913d960fcb89d643`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f22e1bb25c078c9483d71c996108b2df9d72d8d4fb3b918469047d351b101c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210875748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36cd6d1236856d1a317119c3d2394cc9f66a0330fb7e1bc4643b3e2cf7e710a`
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
	-	`sha256:b5aaf2cfcd971df2d03428ee5ee76c3c86e096ad694169897b6600599fa86690`  
		Last Modified: Wed, 23 Apr 2025 20:04:34 GMT  
		Size: 89.1 MB (89091269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66b0fe0a561496071832a1114e4f93cab7b74b4a6a0186734843db320c895a`  
		Last Modified: Wed, 23 Apr 2025 20:08:19 GMT  
		Size: 69.5 MB (69529212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96157ff52cd459477c5557eac0b7a3a77a2f93652ec7e0541fb6b53bbb71191`  
		Last Modified: Wed, 23 Apr 2025 20:08:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b073a7aae2cc032759f84335f97e241af101c25c02e0103271a71c01db78253`  
		Last Modified: Wed, 23 Apr 2025 20:08:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3816240f696e7a4d184d3c0919613920721a0779e5bd13ec6bd1460b3d255b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b661dbdbdff3842f78f38bc7242b42337db67f1372050929b8e2308271dacf7`

```dockerfile
```

-	Layers:
	-	`sha256:0798eba8d4ffed5ca334d0d7c840779492dba4e9891e6921b9d0110e072ff728`  
		Last Modified: Wed, 23 Apr 2025 20:08:16 GMT  
		Size: 7.2 MB (7162243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28c8e097960b644c89c5595ed2d034f9c14bc168022d5e69410d2b1407c13a2`  
		Last Modified: Wed, 23 Apr 2025 20:08:15 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
