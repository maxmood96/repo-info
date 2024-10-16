## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:7329d97539cd2e86e2df0da439807287ada85545277fe08741509cf2347793af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:479ab51b80777d3195328f1ccf2c952d295e0b2f01dbfcb56fb4d7d5ea1f7e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289683521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66f68c00e9ab97f20f19d3269307ba9cfb0ba0c857de721d066b60cc07accb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e2101a93e17cee3361d55f61e2c6a569322289e845b8a04c648ef0679c8459`  
		Last Modified: Sat, 12 Oct 2024 00:54:07 GMT  
		Size: 165.3 MB (165267587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca4c7ff18534cf79fccfd24537aef30c7e2da28a9cf274f83c6d8a36e5dd283`  
		Last Modified: Sat, 12 Oct 2024 00:54:05 GMT  
		Size: 69.3 MB (69333497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719f6b6794391ce5fc1907773cdf22653ad61ac45e25822ea4acafb79fc6c88`  
		Last Modified: Sat, 12 Oct 2024 00:54:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476c7e404883dfbcccf2b65621d28f1e8fc6c0ba03742da32e6992320edf41ba`  
		Last Modified: Sat, 12 Oct 2024 00:54:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e5718b6f7c2ab467ebb9a7616d47fccb398ace1cac03f92a0fb10230c06dd20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4709c8819580882f9b8cb2b8c847bcc2075578484702516f84c959e9beddca7`

```dockerfile
```

-	Layers:
	-	`sha256:cf86720851063ce0bab15b6011aadd721d730b57859f8b805d4143680d1df1a7`  
		Last Modified: Sat, 12 Oct 2024 00:54:04 GMT  
		Size: 7.2 MB (7194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac3177ac4c19c2d329f23b64e9b369b76aae5b5890acdc725c6e33dd9f323d2`  
		Last Modified: Sat, 12 Oct 2024 00:54:04 GMT  
		Size: 15.5 KB (15478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44fa2a5560594350dea6aa49b892c67e4f984801c0db6f5165d9fe211c332db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286454678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c015bef07e7c0f6800471883f00ae0f0edaa189c0c1d908f9fc7227d6d46e409`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc66007fccb5edf87947252ad7999f9ecb41dd40a0be6c9a5a53e8254e22ab5`  
		Last Modified: Sat, 12 Oct 2024 01:34:11 GMT  
		Size: 163.3 MB (163252784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64410d4c70f17c0fab562c0f3d469d9c446a88f58d889a79236c57a59fbc06`  
		Last Modified: Sat, 12 Oct 2024 01:38:37 GMT  
		Size: 69.5 MB (69466990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723970ea76d7fc5e590154b5f5a815fcb39237b563a151e23e9ceadf0c8e6db`  
		Last Modified: Sat, 12 Oct 2024 01:38:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f203dbded6fd1ebbc7e5f9006e7d2ac468aebda7640c5af1a118a2936cdeb606`  
		Last Modified: Sat, 12 Oct 2024 01:38:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8714cdcbd5dbb5f8167ee73b8d6d6c429b9f769d197914b755b5dc20c5b2b09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1bc8b191d54d7d48c231402c00d6c2735699a41d83aef5ec3644d509eee528`

```dockerfile
```

-	Layers:
	-	`sha256:66ba01554a4205ad48145bddbfe9815b55dc8b59094398e2f43642510030a534`  
		Last Modified: Wed, 16 Oct 2024 02:42:47 GMT  
		Size: 7.2 MB (7199477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d994215eb3fd3c70b46cca065844af5187b1b227bfe35f8bf65968bbdab3949e`  
		Last Modified: Wed, 16 Oct 2024 02:42:47 GMT  
		Size: 15.6 KB (15584 bytes)  
		MIME: application/vnd.in-toto+json
