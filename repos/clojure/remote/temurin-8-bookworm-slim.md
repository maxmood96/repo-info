## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:efca167fb3927fcb5d1d01bdd232d4dfbdd0ae0e11cb2ec618e363ceca2b9363
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:102fe090e49de1e3a828baba9d417962311b8c3d09867e16fb8be04c99c6bf3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fae62e9989aeec1524abea4541e2397a6157006d83e839bda97e31ef15fff6`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89a4bf85dc4a1ee75239b520ee99940021ee135d560839154aebb21d3497fe`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 103.6 MB (103611880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7993d4263524f32952dc097feb089a53579f662b7be3a3875b75c4c6ec9288`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 69.5 MB (69482677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640b46f0624cbe025413bf422bfcc8932a0611f470ba939259c15345ffc22093`  
		Last Modified: Wed, 02 Oct 2024 03:56:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a2f629a4a3a0644444e413048c6a437441ce039364f82287e16e2c8efb17723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0330cea9e3edd8ca27dd8924d1789e15eea83153a68dd10dedfc6cfe86f9f05`

```dockerfile
```

-	Layers:
	-	`sha256:067eb28eddca3980abaf47749079156791a9adfe0d62dd6bb2dc6bb8f2c8e2cb`  
		Last Modified: Wed, 02 Oct 2024 03:56:24 GMT  
		Size: 5.0 MB (5017017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e79ab99bc89f16f2075240ae21ae181039da9dc8169cfae53fe51c3ed72aef3`  
		Last Modified: Wed, 02 Oct 2024 03:56:23 GMT  
		Size: 13.9 KB (13896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:afb46f84b9427261bcce200d8c12470d2f17cbd215501822ddc22b88b02bacf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201231361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f988f21a7526d06dfbad8bf6942a5a7d07676840c13ad440f129991a66769496`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db38c7d544bc9420f8ff7f687e5b07cf24567d55f2b3fb2021f82515cc98a878`  
		Last Modified: Wed, 02 Oct 2024 05:26:33 GMT  
		Size: 102.7 MB (102729229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bec6994e3550b4bc997b871cc13dc17339e2a8ac0b9c8a31eb35c42109f6536`  
		Last Modified: Wed, 02 Oct 2024 05:31:14 GMT  
		Size: 69.3 MB (69345118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f2bf2f417cc5df8395e3652dad381d3d56a6f6abd0bdfc931d401ba3dac35`  
		Last Modified: Wed, 02 Oct 2024 05:31:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:556728061c7de56653be5f2f23c1652871cb3b7b0017ce25d244b8d8e299764e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d918e924c785cde005d4e614817a268a71dcbe15acb67becbd2bbccfb0439c0`

```dockerfile
```

-	Layers:
	-	`sha256:44442a18d90c3323a6f71bdf11595ab4eae9f3c9aada07f7e23eca6a8d08db6f`  
		Last Modified: Wed, 02 Oct 2024 05:31:12 GMT  
		Size: 5.0 MB (5023482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:861ce71d9dc0796c887411aa7979a95470e15ce4876a0e572388d5724bc917b5`  
		Last Modified: Wed, 02 Oct 2024 05:31:11 GMT  
		Size: 14.0 KB (14032 bytes)  
		MIME: application/vnd.in-toto+json
