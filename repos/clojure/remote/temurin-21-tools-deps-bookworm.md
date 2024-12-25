## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f26fac753362d6dbc7f6f769424c95bd885d17b4395eed1265e61b7c56873269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:517179d1198d9c2848201fb65ee58cbd6d2d0e49e9ccc35fb10adf85253f061c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286810561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0149bf344a8dee4a7f0c901603637d6572561e6deb95f0423af13b2f4ff8a930`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcc8fe8bea12ef84c9ee9d45ad9bf1cba448d62a029554a198100843d2997db`  
		Last Modified: Tue, 24 Dec 2024 22:38:27 GMT  
		Size: 157.6 MB (157568680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f222d4b2f22d1f47a8fc39f6f2df3f2a75f6f748969f5f18bd285f1865af27f`  
		Last Modified: Tue, 24 Dec 2024 22:38:26 GMT  
		Size: 80.7 MB (80743774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd23d89c097a61882e8e4e083c591f60b314f5b6b929c79260c3566fe4801a54`  
		Last Modified: Tue, 24 Dec 2024 22:38:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b43dab221e76a89a860cb888213798dcf895a64e4654082971129ab1d634c88`  
		Last Modified: Tue, 24 Dec 2024 22:38:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1c7956ff25e40562a7a33c8974808c93e47a1fb8fe81e5a3110d880c5541b25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30950b3815be7d90e543cc829732816bb48431f59025b876083e1c20f8098df1`

```dockerfile
```

-	Layers:
	-	`sha256:ccfb7642302f4a8ae3a75f9b0fb7c709caae8165b00a9eb0c716009c1062e941`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 7.2 MB (7176120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d08dea2c35a9ff1a1baa86d37b5df3023bd6dfb97e5d103995a7cfbe471ab1b1`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bab54cda9e03c45d03a5f55a60ff88ec25b9f6d747e2f30fb3b29a413f97753b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284725106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b010476131ef9deca20848fd442ba50a2335e06a77a725efad5d24bf1105b412`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6583738d9e8001f0b417d24a1fe63be931d7a0a7d674356f040580ab1f19242a`  
		Last Modified: Tue, 03 Dec 2024 15:00:21 GMT  
		Size: 155.8 MB (155793112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8ca3be0cd36566df6449ba7c112bd9a9972fde7ce3ddf0a06cd74b6d300f6`  
		Last Modified: Tue, 03 Dec 2024 15:28:19 GMT  
		Size: 80.6 MB (80605275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2a743966b05fd03e4ebf4528088a28d3785b80fc2d01b999a6fca6642809d5`  
		Last Modified: Tue, 03 Dec 2024 15:28:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da7ffad0221aa9f82bec32a1d816c38f2c0733857696b73a1cb212a92e57dd`  
		Last Modified: Tue, 03 Dec 2024 15:28:16 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0575fe4133c1baaa10822ec6f96bd3c032f4ff3a848fed56f3a1a746ce4e3642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b926bf03a8d31c7db60ca32237564d1502f16b29ca4c06e9ad36fdd46ad7d1`

```dockerfile
```

-	Layers:
	-	`sha256:bda7547fbc8d0d8a863e03b7a9598ebcec0e0e3faad6b50c1031fd0b7d3f2b53`  
		Last Modified: Tue, 03 Dec 2024 15:28:17 GMT  
		Size: 7.2 MB (7192122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723cc6df01be611df16172b6331759409083c7fe09b23db14ec3d53c00a38e6e`  
		Last Modified: Tue, 03 Dec 2024 15:28:16 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
