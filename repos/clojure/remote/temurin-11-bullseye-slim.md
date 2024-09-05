## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:14e0ad07443052efc267ce96a1856466ea00890fcba9c713d9b1e1865f44fa47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:70104b0c012baa7dd9062cb2efbc52b16f3e3ee962a5b9177b1e32dcf9559a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235681695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303917a699c29bf567b17cc288cf381c6b25352bd6a5faf9f5d0111195d35528`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
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
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91f63a854bcb87c9dea7acceb882449ce6b7382af96dade598ded9e4c511661`  
		Last Modified: Wed, 04 Sep 2024 23:07:57 GMT  
		Size: 145.6 MB (145550078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f6c1000efe700fdac3735ecf0ef35894a1660944d9acb2efb44bfa99873e6a`  
		Last Modified: Wed, 04 Sep 2024 23:07:55 GMT  
		Size: 58.7 MB (58702295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a34e30bb21ee72f50deaa7451a54eb64b444398539d951ba3e297a295bd31`  
		Last Modified: Wed, 04 Sep 2024 23:07:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:672a625da714374a42dc6c4da111d78f705513326a388eed91cb71fb21102737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1015e7ceefc7709afafc52579085e8b54ba33a4bca190825bdb251feccb6795`

```dockerfile
```

-	Layers:
	-	`sha256:ee79557faf18efc46fe9f45dcb7f5e3d5163629d0139ffa9a86f03affa680644`  
		Last Modified: Wed, 04 Sep 2024 23:07:54 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbce57adbc50003a11b89ab30f760c0e7063e0fe09d67b858a39d3f845e6623`  
		Last Modified: Wed, 04 Sep 2024 23:07:53 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6fdfc5500ec0ca89ed1003e8e92d54d275f90e5fb7fbec4abb7c8c66d7e19fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231131175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab12b2ebe265ed9a85498751e84c7b835835e44c0f1fabe1d5885555384b928`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97190d565d6e988e1267474ec2deb103d496585fb03fad3f32525640389e705a`  
		Last Modified: Sat, 17 Aug 2024 06:04:04 GMT  
		Size: 142.4 MB (142354792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06ac6ba42cb478d5d8822f508ae780ec3d85b2fd0bb866bb5da215c998bc96d`  
		Last Modified: Sat, 17 Aug 2024 06:08:56 GMT  
		Size: 58.7 MB (58699651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b086ad5b5b18708389f959edeb3874ce3e5749fa77e6ed7dbe8a505a337f15`  
		Last Modified: Sat, 17 Aug 2024 06:08:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5f08fd8fbbd4e8cffb4ea8bc05e3e66ae148e9bd6b034318182267b8e95abfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd31a031c9555b11049ec7ef9e13fdd07519fe77fca584f87c5dc08eb054a5f5`

```dockerfile
```

-	Layers:
	-	`sha256:d54727e2e4f56fa1f2348cabe35b3f1f5bc6e12344ef37ff08bba1f35a9dfb02`  
		Last Modified: Fri, 23 Aug 2024 23:55:39 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d566d4b8b077d4d7dfa3aef648d8b154d098f4c29e7f615499dde0431dc0a184`  
		Last Modified: Fri, 23 Aug 2024 23:55:38 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
