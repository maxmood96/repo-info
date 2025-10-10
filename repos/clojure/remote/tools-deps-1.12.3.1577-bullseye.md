## `clojure:tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:366bdead2134b6d4dd96cbb414431a8bd07584dadb1c3e6fe4a5021df272e2ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:72f25dc8ae18990d85f864e9de5bb01d08ff527090fe484653eeb22e98c7d6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215353982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996c6b08ce0a9a76a5ce4145cbffa8fbd7c6b81c3e1b59dfc1b817c7e76c9382`
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
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c555b2230abf9528d4dab2addbf80dbb226fb52c03cf9a99d6e1f1a371422082`  
		Last Modified: Fri, 10 Oct 2025 03:54:30 GMT  
		Size: 92.0 MB (92036030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9169333745dfd320c50902672e24f30a7731567f3f73ef7aeaefa0812eea3ef`  
		Last Modified: Fri, 10 Oct 2025 03:54:27 GMT  
		Size: 69.6 MB (69560849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b492e266ecb4a75f5bd2bbf6eb4d2a7f4b1406d32a07fb23f717882461264b6b`  
		Last Modified: Thu, 09 Oct 2025 22:37:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fde7095bca527016593e8c206de337b7ac46b1b18eb864df4884c6009dd33d0`  
		Last Modified: Thu, 09 Oct 2025 22:37:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cfb86ea7c26c66affb79038a7cc7711fd82aa923febdbdde26f46de8643e4d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7365107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f67fb001e121cbe2e9d3de99492848e0d56693265ad7db853a2141f3252eb7`

```dockerfile
```

-	Layers:
	-	`sha256:612a7c49e257d55f6affefc1ea7be321f2dd3427a8517e250baf73cb25227d01`  
		Last Modified: Fri, 10 Oct 2025 06:47:22 GMT  
		Size: 7.3 MB (7348617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ecc2d8012890e62a74e656ab4cd0d0e6a5920663eed736f88918dbbbeed72e`  
		Last Modified: Fri, 10 Oct 2025 06:47:23 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c49e347c2038e61b89de1a9b1f92c0af276cb89654505c349ea7278d417b28b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212991828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6edf55a5de3165ddad086b94c7f154b1a5212830d95e897085e28eee62059d`
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
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07183f516e4baffa294c3bfdfa020f8f381e5071c0056f4661738f275186a03`  
		Last Modified: Fri, 10 Oct 2025 03:32:27 GMT  
		Size: 91.0 MB (91045228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef2fe8253ebb1d3d585bb78457d7f6b5c256e8cd4487263aa5226b53b68ebee`  
		Last Modified: Thu, 09 Oct 2025 22:31:14 GMT  
		Size: 69.7 MB (69688145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d39182c505b02ff3450ae1914f52d3cdd13dd779780a35a85faec6992d8d8a6`  
		Last Modified: Thu, 09 Oct 2025 22:31:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a6670dca083783b280a09bf9dd2f90d18bfc8aaaa73cffc12c66cf4a51cea2`  
		Last Modified: Thu, 09 Oct 2025 22:31:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3fef8429f02b56903df9d79d7930b7b2235718ee0a1270b8f67ec737e7db4bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7370369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28646e54085ea2ab66b07e5c8f8b5431a66e71d537c4e72965643860898e5448`

```dockerfile
```

-	Layers:
	-	`sha256:dfafc30c8a69af5819ced50b9ca488ab17028ba91ce871ce84a97475a4656b2d`  
		Last Modified: Fri, 10 Oct 2025 03:38:43 GMT  
		Size: 7.4 MB (7353737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc2317420dbea688b8991cd5438051b3a8be8eb3b184f5bcbda73eac0e574f3`  
		Last Modified: Fri, 10 Oct 2025 03:38:44 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json
