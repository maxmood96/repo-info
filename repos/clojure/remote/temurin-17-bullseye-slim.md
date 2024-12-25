## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:005bdae3668dee985324e3b0596b391a46ef862ea6e84d83272236459a86a4f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4eea9b48dd5693ea6fb3f3705b9d19a5e6006ff1b01b7de179a39e562fed904b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233546543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de18e022f93f7ad04313d880cf1ef18ecb4325848f49cf621e60babdf0475f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81c45a1381f1b13fb99721e6135efc8f438bb50685df2541797ed6845134bc`  
		Last Modified: Tue, 24 Dec 2024 22:38:13 GMT  
		Size: 144.5 MB (144536674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc96d6f9c57489ff28e14b6a46439f321fa65238d876f8366bfdc83d63f45e`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 58.8 MB (58756188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ecdfbf9d9c6575d4461be5b2bec318cc6ac09e5065b986fa2204b30257b56`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4985d479ff3fdbe74c080d082abc04f93197455711ffc11023e5672f86272d`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ac91f1d5e6056963d0f6e11e8a85cbd9d4380165183200c0c8f3344b4ce47de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6aaff449e92038ccce35ffc4c218fabed2ba426792f42e2979e8675f3131f8`

```dockerfile
```

-	Layers:
	-	`sha256:eca6f1363ee2dc80ba0905e208c17b19b9ccc20b90bc37302cce21f4fbf578cc`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 5.1 MB (5117007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:557add435ba0713900cd90d8dbeaa4ace8c415ede99ffbcd7386da2acf97c4e9`  
		Last Modified: Tue, 24 Dec 2024 22:38:11 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e16cf635d584757de4bdc8f7b0eee470c59b894920a6d2bd65c08d1d9ee95151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230987058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3910279b6f93365dd9b7f785690c50f3a9a8a76e7036ea4142ce71113baacc2a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72214e6bfe3c826c0c4a84f416735135366c7c14e21b789d9e9876fbf8e87e1`  
		Last Modified: Tue, 03 Dec 2024 15:23:02 GMT  
		Size: 58.9 MB (58880137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63fade85b7cab6ab3db1bf6eeca5ab1dce3689a8b736b0f3d97f59d6c906a91`  
		Last Modified: Tue, 03 Dec 2024 15:23:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a058f49ca4ccb5976da34b0a1c6cf68ba31274966e445337d060703b62d2b0f3`  
		Last Modified: Tue, 03 Dec 2024 15:23:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f8bd4b1ffa04bd0116dfb02b51ec3dbb5e611e3785a5770641eca0450d70cb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969fd941a13ee2f5ee10b4d508bf91640bebca514de8f90ee9697dcd5c1a3985`

```dockerfile
```

-	Layers:
	-	`sha256:680a60b30336007240c680fe4cb87609b8b7118fde738114e8e7f3dd938e359b`  
		Last Modified: Tue, 03 Dec 2024 15:23:01 GMT  
		Size: 5.1 MB (5129286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89356c86ddeb3ca6b6363c4a4421624a2e64f10a00502feb4d6581d82e04cc41`  
		Last Modified: Tue, 03 Dec 2024 15:23:00 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
