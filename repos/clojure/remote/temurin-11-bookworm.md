## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:9073277762d8c6e915b1a323636dda036901b20f695f13adbda7248c4ab4898b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:631b5fcfa00e20fb9cf6352822048121f3b59fd3b2ba71f1daf753e5cd5668a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276033845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5754374b58016498d3cd0447f69b7a8a3a47fc16958e66412d8f6ebe322e2800`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8fa932ba7ef46009bec74959f493d9dce47c3678ce738df10a4d123315c5ac`  
		Last Modified: Sat, 19 Oct 2024 02:55:46 GMT  
		Size: 145.5 MB (145549919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3554796ccd1e2e79e9e2f99e9833262fa9e11a7b1a26c91455a10d995ff2344`  
		Last Modified: Sat, 19 Oct 2024 02:55:45 GMT  
		Size: 80.9 MB (80928258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedd12b730f8cbfc0cc61340a0ef8202c6486c554621785d519f8f23ea37c446`  
		Last Modified: Sat, 19 Oct 2024 02:55:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5b0163f6836644bd9eddb81ef8ba2d7dd1c9a08daadd3bef3af52d6c41753271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7216629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a45e12b4b5a72499926cd048922ef87bc3fdb43096b65f53c614877a44e78fc`

```dockerfile
```

-	Layers:
	-	`sha256:5e43c34621e6995067c9603a2cecf7dbeddc78c357a8fd7ed6481c172222eee4`  
		Last Modified: Sat, 19 Oct 2024 02:55:43 GMT  
		Size: 7.2 MB (7202558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccef56552119a26ad73c91bdde281ce16c7182cafbfce5e7fb2aa74995666614`  
		Last Modified: Sat, 19 Oct 2024 02:55:42 GMT  
		Size: 14.1 KB (14071 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:349f8e4b1453628c92ae5ffb98f3c9f2b83e5b940fc94996b860d2df048b80bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272730629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4249129316f1e9596045ebf2cfd067e15e344e5182e437cdec406b54d668148`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e112fccb06501d78425de14a7cad0e916a7b2ff8acf9a5f1680aa28c73367de2`  
		Last Modified: Sat, 19 Oct 2024 11:48:35 GMT  
		Size: 142.4 MB (142354833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22898f5957d72150694e2750061367f2053a21c956c1b3dbabc59f01bfd823f4`  
		Last Modified: Sat, 19 Oct 2024 11:54:07 GMT  
		Size: 80.8 MB (80790172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b03c532468338e4c1202949aaf5bc8e4cf12291196a73861159b02216cb395`  
		Last Modified: Sat, 19 Oct 2024 11:54:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89f132f9c81b05f48b2e9ebe7bba617d55db6d82810951e1da6ade98587ac651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7223127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfe9fecc75dd15d15045893ef42d0e8c0ef97b5939d1e5927236855534ff96f`

```dockerfile
```

-	Layers:
	-	`sha256:fb9a0cb83574ddb1ea351cc05675c5c33fadd131a7daec1c7d7e15e57fe4c8de`  
		Last Modified: Sat, 19 Oct 2024 11:54:06 GMT  
		Size: 7.2 MB (7208945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53c9fcc1eae89abbda273c2d0df1ce877927e21e32b86394cebe3641834b049`  
		Last Modified: Sat, 19 Oct 2024 11:54:05 GMT  
		Size: 14.2 KB (14182 bytes)  
		MIME: application/vnd.in-toto+json
