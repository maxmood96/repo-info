## `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:6241e385a90e9b7a223ae004729fe3771f576a901c98e82fa3e7ab1108b6b4b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:82e193547efb1738f4df4659bba006ddfab07b191171213cb00b4ced1fb9be1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248949781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7b6e5108a49b9d19ffaaf385709140bc3fffaa25867ed4fdecd0699c413ff2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92caf91f7fc939229432ac3b0d3a5dea5db5a63dfc5d06d9df168542485be91e`  
		Last Modified: Tue, 17 Sep 2024 01:59:01 GMT  
		Size: 158.6 MB (158579306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1573a784346c24eab7c60d1241ed568bfe70b31319c45659b66b4be0e534d5`  
		Last Modified: Tue, 17 Sep 2024 01:58:55 GMT  
		Size: 58.9 MB (58940754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed07f414f79b6ace8317fe136feeac923156929b925c356347a3c1f7f50b44`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f641054f87e7db160fe32a665257514ea0421aa4d6593fc291668b8112a94b`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:472721e0b4102882fe5362ec3d7071166445ff3e0db333a0a85a177e76ddb0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07790ec226b807621cf285aa4ad16d04cee959222570b53bf6be5c3d8771126`

```dockerfile
```

-	Layers:
	-	`sha256:cddb93abd3e6581c8c04d1d6dc0c45fa342f58cdff3de9f7ba88f25637b98d22`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 5.0 MB (4950532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7784c8e04800ed839394e2e9be3d0534925427a6e195b3699e0d620cbea6cb29`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e7d20328db9acb0dfda336d4082a4c8bbacd4f1df056116c2b146de8a28af34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245893263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86ea3f7157aa32439908681697ec8d608828ffdff1143a73165750401842a63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856860e2a47fccc971712d86611a293ae710dcc38155a07f1998f80a97cc47f0`  
		Last Modified: Tue, 17 Sep 2024 04:44:04 GMT  
		Size: 156.7 MB (156746196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a453e3b9086df29016e8e02c7cb22d9859892eb900fec76fe26e27621c5ec`  
		Last Modified: Tue, 17 Sep 2024 04:49:17 GMT  
		Size: 59.1 MB (59071658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40332d7252dfcf44f8297c517ea0b46bf27da166a8e2ab7ab83983822c31c09b`  
		Last Modified: Tue, 17 Sep 2024 04:49:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7114ad1f3cb59f46e5c675b3d1569865ffbcf0ee80b414eeb95bf2ba1c847e23`  
		Last Modified: Tue, 17 Sep 2024 04:49:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b03b8de1fb7e7bdc2aa1fd6f90eb70673132658b95f7ea0783165e9377d97c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da0627891d289bbd34412b22d38c2049bcb20c84f1dba5bec52745243cabc8e`

```dockerfile
```

-	Layers:
	-	`sha256:91f914b208f41f16fd06d5850561c68b41514691ebd47394165bd3ecdd010e3d`  
		Last Modified: Tue, 17 Sep 2024 04:49:15 GMT  
		Size: 5.0 MB (4956912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e84dd5a64be2b52fbecac2ff7261c8ff21bc8d3759b44f45063649986ee41b6`  
		Last Modified: Tue, 17 Sep 2024 04:49:15 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
