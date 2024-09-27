## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:09db6cf1b3213773626512cc47c6dcfbe71098896c916073fe44248a38161608
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:07d8dc42224be0b2ca3d47982fe9790cf71270dea3c9fec6061c7580ec4dca58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269582896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced053454b50e5ac1dd56e2c9e8804fb58c23f6b861cef3c0a12226425e832b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0802f6e65463207e14af6c4a3f663aa71de5172062c4e503456d7c354703ae7`  
		Last Modified: Fri, 27 Sep 2024 06:01:15 GMT  
		Size: 145.2 MB (145166556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0459b2be32d71f3d3ad6f7eb83fae32d85c4c02ad89fedf0990b88917e67de`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 69.3 MB (69333910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eedadf8de3560c7be0cb03c66b6f5137fd923611ef2f1350b1c77b2618e088`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c9959795dcb4f2b194a8e3a567e1d772d916fde0b8f141a1194d35eb8ce8c6`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d5b74ff078581432868a1f24e83ad3d3301fe70d073dfab288f58a0ea0d7418b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fb1d333eb18e9e52671ef35ed8743be16e6688ad850dd93652244a06de6e8d`

```dockerfile
```

-	Layers:
	-	`sha256:1f8e808d3ef21a5c7123ac5f52ee4f386490f0d16d7c07a95e6010ac468fa616`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 7.2 MB (7189327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d65d1f9041114be9f16aa3e757120452d9f9cc2186bf4d917208a853c173e3c`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9baecb3a7846addad3138e439951bde81e7714c218d2b4f01abb09e4d2e7c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267161010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711b616b8cf35f1c0f730d0a112de3ceaa0a085b7ba88e4a467aa184995dbedc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c8e38c80fbcf665a8abc90c47c8f309a66959e0c3e33e66f963837bf6c6265`  
		Last Modified: Fri, 27 Sep 2024 10:34:05 GMT  
		Size: 144.0 MB (143959461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2e19ad5745a3f62219cf37c49df1b5170695e23a0560450c4ff686988a4cc5`  
		Last Modified: Fri, 27 Sep 2024 10:37:48 GMT  
		Size: 69.5 MB (69466648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9ac71f5b9f061e21b1976cd455daf4df9b07b8a5fbf07950215fc506ecb869`  
		Last Modified: Fri, 27 Sep 2024 10:37:45 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbda8b338b775752fc862113988d751174b2e3a119fe9b617150c2160d62ad86`  
		Last Modified: Fri, 27 Sep 2024 10:37:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cc80c45b412739dd4a387a6bb12d45e9ddefb46c1cba2f850a8b579d8da340d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38d1769bc99b56bbe08a605bc105641e4dc32d8260703743a8aa4d6b6f528ef`

```dockerfile
```

-	Layers:
	-	`sha256:c44cc22d02f3249890a9d18d8ac6f8b9cc652494bc70b032cf0627ff5bdbc8dc`  
		Last Modified: Fri, 27 Sep 2024 10:37:45 GMT  
		Size: 7.2 MB (7194430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47524d2d24f89c3692b37d1b6d4e7f006437f187a903e2894ba37f10d1e6f8d0`  
		Last Modified: Fri, 27 Sep 2024 10:37:50 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
