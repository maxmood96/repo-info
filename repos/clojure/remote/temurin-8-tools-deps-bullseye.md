## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:1755b0c0ae2f809800772447550ce01a3b6adff9d599ba1ba6b359358d5d7b18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fd9b940e6f48248ff66539024fe22fe15cebbe6d3687bb9a031688ef5aef98e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228027645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cae831ecd8f34d93cf6012c4fb12a5fb42fdf5b5c821a36724108c0bb1270a6`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228e2be12f7f6765e778debbadd879f4e3b499214529203fc62e327e855251dc`  
		Last Modified: Wed, 02 Oct 2024 03:56:27 GMT  
		Size: 103.6 MB (103611902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372ebd4a54b822ba55e591d83bda7eb33ca3c1968e6179243123f66b243fd50`  
		Last Modified: Wed, 02 Oct 2024 03:56:26 GMT  
		Size: 69.3 MB (69333706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640b46f0624cbe025413bf422bfcc8932a0611f470ba939259c15345ffc22093`  
		Last Modified: Wed, 02 Oct 2024 03:56:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:12404b7ef2c5e7bff63a7acdafa25eaae779c40b11e0fa93a3d82495f157ab2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483e4da4f52f6654015643cbb723363fc6a848412b0edc8929aa8150ed4fdd70`

```dockerfile
```

-	Layers:
	-	`sha256:28de25e3d5236777594ccc98dd5154593814740e894cd69ecedc02e859d4d18b`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 7.3 MB (7312169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88e29ffdad6564ce238633e1371a305a3b89a3b1b79bc322b78c508cc156fb52`  
		Last Modified: Wed, 02 Oct 2024 03:56:25 GMT  
		Size: 13.9 KB (13857 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a46678e688fb19cc95bbf0c0b4356d15c5a6eb639e3c53a32af42397a48668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225930644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf62c5283d6100f086a3e11ae4257ce6fa6d4951e18a5a8e9a5449532da1f9b`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f5ae86f098e723094a195c93eca7d5c66dd86597c4b0ad1116bbb60b4fcd81`  
		Last Modified: Wed, 02 Oct 2024 05:27:39 GMT  
		Size: 102.7 MB (102729229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f6c54a4f7af6a355282bdac74a65b573835881a74aa7479956c2558879b9dd`  
		Last Modified: Wed, 02 Oct 2024 05:32:37 GMT  
		Size: 69.5 MB (69466906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66853e9a3abc628de80bf71819d54e97c385f507a2e336d558e6435f294806aa`  
		Last Modified: Wed, 02 Oct 2024 05:32:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f77965d95fa93daa45afa4a1a74627794f6f609beecde0baff7a029efc9f08a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7331934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a234ee468e833ea90a4cb46f0e4189179021c9c7af35b41dc2c64a631937b9`

```dockerfile
```

-	Layers:
	-	`sha256:74eaadd0fa407504039afd7e634e9352b27f071f1e56018db12d05d348a019a7`  
		Last Modified: Wed, 02 Oct 2024 05:32:35 GMT  
		Size: 7.3 MB (7317971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023eefcd164b64214c8534c570d4883f981f3d5847c1817d5306f467a19479ee`  
		Last Modified: Wed, 02 Oct 2024 05:32:35 GMT  
		Size: 14.0 KB (13963 bytes)  
		MIME: application/vnd.in-toto+json
