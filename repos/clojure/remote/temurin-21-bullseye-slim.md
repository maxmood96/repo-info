## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:9bbbdda800a66de82801b6832b4eb3810231e76c8f7698d0f5ad0799a4d01d45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b8d1f03af3a182ad4172e9f93ece83f9fc6b54594b7c2f442df06f32bb500a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248949027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a2e6e7dd2c7fc9d71aa3a492d7188237ea8c86fad4713564b68153fc753928`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac98895f371c0ff96a0d1a56b45bbfecca818e4b2e9352ba79d4be228947c68`  
		Last Modified: Wed, 02 Oct 2024 02:58:06 GMT  
		Size: 158.6 MB (158579254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb4f887c535906d29930697551e1c302edec6b11312fcbeea39edcca3e35cc`  
		Last Modified: Wed, 02 Oct 2024 02:58:03 GMT  
		Size: 58.9 MB (58940135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71718f47574c9bd3934933ae7de5ed1ce291b430fa90f2992e71e15e8862f711`  
		Last Modified: Wed, 02 Oct 2024 02:58:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d61371260fd65b6799f30a00584051ca083a666ee1564898fd9b16b9f3cdc`  
		Last Modified: Wed, 02 Oct 2024 02:58:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73a9586ea4694ff048a32b73330ba68df8494ece493b021abda4e22b01a10f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e43b0bb5ed7b7fac00e6ead541d7600c3c3ac5add013d4864101e68bb8d80`

```dockerfile
```

-	Layers:
	-	`sha256:ce1e9b09c9fe32e32705ae3b69abeb38e96e5c25498c9c14fd73ce31610406cb`  
		Last Modified: Wed, 02 Oct 2024 02:58:02 GMT  
		Size: 5.1 MB (5103282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41fe140676f4f8432686770e34fbd8e778b0d8c8beac0af38d1a682a8059c028`  
		Last Modified: Wed, 02 Oct 2024 02:58:02 GMT  
		Size: 16.2 KB (16214 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d4428321d6d9304f9a381d145c8b9826a0acf1e8abfeb4745971940a6a3fc5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245895776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e0087b7ac957566564db813a0ec8caf5b545b4a4255faef881ddf1579e2050`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b57daa2dc81520c3d5517e123118ebd22f17a64e012dd5bf35397507f13d2ce`  
		Last Modified: Wed, 02 Oct 2024 05:39:34 GMT  
		Size: 156.7 MB (156746169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc36c3f84cbc1c8632592fcd714864399966f8a1c8c29511f31e89abe8a4f15`  
		Last Modified: Wed, 02 Oct 2024 05:44:03 GMT  
		Size: 59.1 MB (59073406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24196ecc2c7eb1381a06baa5ab932826f408fa78c25eaae36f7b5567a6c13d2b`  
		Last Modified: Wed, 02 Oct 2024 05:44:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f9bc625987f76ce36fbd7091c410a8ba4d25fbf731e766dc7cbc92575a1e53`  
		Last Modified: Wed, 02 Oct 2024 05:44:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:307d9ad3b6af5def4037d58b57aeb34ec3ede88438983cad9dabb337b80556a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdf10c3128690ad0b60ecfe590168502f59170a37e643794e45317cb7158230`

```dockerfile
```

-	Layers:
	-	`sha256:373b5cdad21238634c80518e472c34e31307d8da7ea07a488d76a297dc9fe706`  
		Last Modified: Wed, 02 Oct 2024 05:44:01 GMT  
		Size: 5.1 MB (5109043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0eecffd11880ba5db05629b891374697a4ac6517b26996cf14ed7853124ffe7`  
		Last Modified: Wed, 02 Oct 2024 05:44:01 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
