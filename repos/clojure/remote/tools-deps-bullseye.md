## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:0047af04481fe1dfb2dce446d467c4bb7acbead0d444e5c5a6e37d007430b0aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:eee618249441e9b01c62a968df2a618be542ee18d7a27f3ac6939d58bde60ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215352856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d7c80cc70a11a9d02486cf8dc3471626be0dbf01ab7bb65ca247dcfec6693f`
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
	-	`sha256:cd5c1ae2d04bb99d066271e9ff9c604e455022d4492a262ebee6a239483b151e`  
		Last Modified: Thu, 02 Oct 2025 09:54:26 GMT  
		Size: 92.0 MB (92036049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9249162e8d0f299c4d06715fdedf389cfbcbacf818e15aebe50bb6df0a2f3ea`  
		Last Modified: Thu, 02 Oct 2025 09:56:07 GMT  
		Size: 69.6 MB (69559701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94af8fb195ec0b485654c14b22fd3817f65ed9661f0f0a3e8961c0801b9b1f48`  
		Last Modified: Thu, 02 Oct 2025 09:53:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6784960800bdf4f5e4bd815318ba9b19762706e68ca2297b358929902114f202`  
		Last Modified: Thu, 02 Oct 2025 09:51:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5ee9f57d185700cd885dc122db67ad837a5a38c3025c3b5f9c9efde76ccf3824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5601ec999343d57789803aaf8522e40f6a6ea1c04597e7d6d022c31c96b983b4`

```dockerfile
```

-	Layers:
	-	`sha256:97e2308eab4b13cc0c2d26555d8866593c97ca858e5069d79f7a3d12db73e3bf`  
		Last Modified: Thu, 02 Oct 2025 12:44:09 GMT  
		Size: 7.3 MB (7346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba37b2f6001ee903de449adbe4b57879a27f0af6c8b3884db808376f359102af`  
		Last Modified: Thu, 02 Oct 2025 12:44:10 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:tools-deps-bullseye` - unknown; unknown

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
