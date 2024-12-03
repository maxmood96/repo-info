## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:066493b11ad3338e763e80ccbfab373ac4dbf48eb1520668df62fc3a5406e004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:5f87ad646c2238ed23977563136582e82fb8d44fd265dfa6d7a926f16bc8160c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286810830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fba93d4ce5c91da4ca08c631a0e5c66269fa601e5f451619dfd4aef676fe2d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa67108817ecd74db35b696c24dd97463a4ed21463c8c82af2dd07d386f7b0c`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 157.6 MB (157568687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb4e698fbc08374e868ab40f75f459668759b3cd56880345aa6f08c749e8ee`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 80.7 MB (80743896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b629f1a5aea11e490e64c6c46b551c82ceec56db8537fcac3fca9672c802187b`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5023b770804ec7cc9048b3788c7ca0965028456527975797cb5514e9899c7f`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:1675c9b1ffe88daf2050d95675826bce4cfa60443791ea8ca196df777681ad1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11299da3b28fb4e770716bb629ee0708ca2f116b43f2ee95bcc008e46d92e26`

```dockerfile
```

-	Layers:
	-	`sha256:4f2263dca4cb6d459a3b8fbcf3fa2e15a876b86d15802625de9c1a3f39f77a86`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 7.2 MB (7186282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e478e03632f58ea9ec4c121a885a21a41b58cbee4b9327a2d8c828881c07da`  
		Last Modified: Tue, 03 Dec 2024 03:25:47 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps` - unknown; unknown

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
