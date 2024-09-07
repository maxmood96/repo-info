## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:7ea4b6b464a5c1f233e5f702985bb9d013f594ef7e1a9d4d774a26bd56f14ca6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b0a26c106dc4fc23de7350e5916b4cc93009a6b70153b587c371d7528b653911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288836048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2061c1bdc3c29af7679f72c7da13dffe75e32c60e01607c6f8b8146e9ef0deee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86d4b61bcca07b96e592990b1c9d110a3c39b76fe1f37a8ab05e74640af7d8`  
		Last Modified: Fri, 06 Sep 2024 20:59:43 GMT  
		Size: 158.6 MB (158579262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1e844fed39adfea607efce9342263b5bbfabc9d74fbe0155bc463bace42b79`  
		Last Modified: Fri, 06 Sep 2024 20:59:43 GMT  
		Size: 80.7 MB (80699044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42251d2d0caf3eb0df26605788b80f354f4b539f75d97c3c91964fbdeee4ce92`  
		Last Modified: Fri, 06 Sep 2024 20:59:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950a2b61b7c0d4997d320a6660b932db82267ea929a1d24fd654ea4edb4e1e9e`  
		Last Modified: Fri, 06 Sep 2024 20:59:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ae0a88cf0b639ca7ae407e5c4b27372f9d43317971ef49b2a7cc708d2106f13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c841558e4f56e112c7ff9feccaeac25466ecc9df3076d697a4e7075f215035`

```dockerfile
```

-	Layers:
	-	`sha256:c064931d8f177e08be1d102a9bced613657461dc94573ad4f75363fba4b8ad3d`  
		Last Modified: Fri, 06 Sep 2024 20:59:41 GMT  
		Size: 7.0 MB (7001481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e88f812494523eaccc6f9878ee7826d8715a9a41c8fce8a57ad0a3b96bc0a43e`  
		Last Modified: Fri, 06 Sep 2024 20:59:41 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc4701360f02c9c892f755da60dd79171532f5d640cdb495bd0ed5248dc722d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286780241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d498284f2635e8474f61f743615811934170bb31f96a19508ff118ca2245211f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b46fa0b162a627a54ecab3826334bb069c39d9832f52c5f8bd1d7b58c992c`  
		Last Modified: Thu, 05 Sep 2024 07:46:58 GMT  
		Size: 156.7 MB (156746214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77289f2bbcebb0162ba4ad37bcf7179c1c45b2d2f5d3f341fe077f61d78a5acf`  
		Last Modified: Fri, 06 Sep 2024 21:36:28 GMT  
		Size: 80.4 MB (80447364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137f2ae153e8e83b2a5b5897bd3f18210447e9d0c24cc9dbee4b1c49a09b5f66`  
		Last Modified: Fri, 06 Sep 2024 21:36:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e94321c99e50378ebabb205311038064687979b8a1bd3c9e6b520445a1a662d`  
		Last Modified: Fri, 06 Sep 2024 21:36:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:42f71dad2f525dec10de6ae8af1ed2ef58ac07bad1f4aa6bf0d51a90f5168379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7025988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a78b43d3b583b550870695e69b1630daf7f7e808e25f19a3ee76fedc31377`

```dockerfile
```

-	Layers:
	-	`sha256:ee1aa62efc0edb4e349f3403c28a6435e09ebfc811a9ae371f2750aefac07e0a`  
		Last Modified: Fri, 06 Sep 2024 21:36:27 GMT  
		Size: 7.0 MB (7007940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c7d22cec2995e0988afe8701e25a6351944692a679e0e880a19f7bd57ba5d7`  
		Last Modified: Fri, 06 Sep 2024 21:36:26 GMT  
		Size: 18.0 KB (18048 bytes)  
		MIME: application/vnd.in-toto+json
