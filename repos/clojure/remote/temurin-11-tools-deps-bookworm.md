## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:0e260e5f25594e6eab02b81696f09b6de2494aec11092bf95d7324ff31ea3132
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22794abf9850dc42cf087e7a4caa7132523e63afbfc4a5caed6425500c26e046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272732445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c7815208d8c1accd8d1528c55ec5c45fd6d70486bc053cb061bf037d3a2abc`
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
	-	`sha256:a37fe4b3f26ea0b745d94ce1fca7f6c7322f18dbef079c4b027c82bbfb40ef1e`  
		Last Modified: Thu, 17 Oct 2024 08:03:37 GMT  
		Size: 142.4 MB (142356628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8601882a8e10f052cc2d2dbfcea8fb0ce24e7411f6150418037c9ca0ce9f49`  
		Last Modified: Thu, 17 Oct 2024 08:07:48 GMT  
		Size: 80.8 MB (80790196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7296890fe087c49c3313d089e89bb58fdb911a598c0c5c44d999810a5e8e5705`  
		Last Modified: Thu, 17 Oct 2024 08:07:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6d7b7e4502d190c9ba90596b714d1ecbf9a0380972b3283b43ff96d8a8400948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a4dfbb8815e8687678070a179cc8245af9db1294a2ee9e011c8a30c4ad60e`

```dockerfile
```

-	Layers:
	-	`sha256:1103d1d01d58f9f32ea235b06937ae0bd7a2a6580d77858ed485e85b5a4f0618`  
		Last Modified: Thu, 17 Oct 2024 08:07:47 GMT  
		Size: 7.2 MB (7183200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06584a670674ebd3b133fad108f25fae9979fe85590de0978397b71c5cad7ab5`  
		Last Modified: Thu, 17 Oct 2024 08:07:46 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json
