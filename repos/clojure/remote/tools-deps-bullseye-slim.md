## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:4a74185fa6dc6d8fbdecce240b86e7171266e03fc73d556a0ad5a2830ba6d544
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:18661dc73af913ebdfca339c108c08d40bfd8ed3cfb8a886b6d25c6d157b5bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181445878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57103d6dc2982bf363dc344e158d556c80002c3e4c9d5a7d4801e0761d4289c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5c1ae2d04bb99d066271e9ff9c604e455022d4492a262ebee6a239483b151e`  
		Last Modified: Thu, 02 Oct 2025 09:54:26 GMT  
		Size: 92.0 MB (92036049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c45164088a90e619b6c33e468a302fad25ac543b24b14ce2d44a6b7fcec1aeb`  
		Last Modified: Thu, 02 Oct 2025 09:54:11 GMT  
		Size: 59.2 MB (59150428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39530de36853ad42d63078b34d1313b0800a1eb3cd0901e449abe6eccd1b35f`  
		Last Modified: Thu, 02 Oct 2025 09:54:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c62cb38ef6d643a8dc490f893a1f406e27078cf9b5d02e5d18deafcf494da9b`  
		Last Modified: Thu, 02 Oct 2025 09:54:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fdf644b014a7acb09de4b762999b81b0620f150cafb878fa8166636afcb8811c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e382d858f58f498cbe3f3c4d5e49ee2b5cea0e82dedd416b66634b680e9cdc`

```dockerfile
```

-	Layers:
	-	`sha256:cff6eec881e8e781a76847a27d8071d708115bfca8a39f626d0aba2b558234a2`  
		Last Modified: Thu, 02 Oct 2025 12:44:15 GMT  
		Size: 5.3 MB (5259413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645baf51f5b8445ec79d1f2244740804ce05e6dbb83af2cb58691d03e9996ee7`  
		Last Modified: Thu, 02 Oct 2025 12:44:16 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af0d35b7a7eb742d9672dafb926240d23da138c7e4fd0e217d9e76b742c793af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179079401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab295a8d63d33b613883b4fea207484dc55404b589764b6809ef7510b46111f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504d22ff1fb40117829704e93d807be5ace6103abd027bb5647173e12d08a054`  
		Last Modified: Thu, 02 Oct 2025 02:47:27 GMT  
		Size: 91.0 MB (91045293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f9b1c297bc669dc5766bb4d14de937496cda826289e71d180ac12518e68a01`  
		Last Modified: Thu, 02 Oct 2025 02:47:25 GMT  
		Size: 59.3 MB (59284643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e83e9da45bd3db13466f3845efe303c3d7958c2a478d753d2a4efddf4a35f5`  
		Last Modified: Thu, 02 Oct 2025 02:47:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8936cd24211ede9478db57b7f70f836c3136402f0e0d011042220626c702c2e1`  
		Last Modified: Thu, 02 Oct 2025 02:47:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:228b9cd0a5ebe235953b0465fd303482c57c362370b4b835afc82c05eb277a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05296f605dc434bb8718a8c0d75e2cd37729eb5d5c2b5a2ad487cab33afe255a`

```dockerfile
```

-	Layers:
	-	`sha256:5becfad255a319c8cf07e939b21a452909d66ef85532a592c5c909cf151606bf`  
		Last Modified: Thu, 02 Oct 2025 06:46:15 GMT  
		Size: 5.3 MB (5265166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:412a0324567f6e23c4e30e0faf101fc92de201d7034ac9083adbca6318a55368`  
		Last Modified: Thu, 02 Oct 2025 06:46:15 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json
