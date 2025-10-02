## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b0fb9ed8e6afe868fb201b52f200f111c22edf5f1385bcb2aa21d4a0b5e99a9f
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
$ docker pull clojure@sha256:f96ef539810025f9c8e40c0a37fe237f9f9b221c2dbe988a98ca6a853e657fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212991334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f9739a026383d5d5dad9e5402f6463e77d2d997e78013e3fa927134077ff06`
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
	-	`sha256:a5ceef1ba97bf495f0b027810b5d7f754bd7a5724301386215c34e936ec1168d`  
		Last Modified: Thu, 02 Oct 2025 02:47:29 GMT  
		Size: 91.0 MB (91045293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b302c3861eee9f74afe286ef3cf0c0768c51b18fbc99c23a9d33163b8b33c0`  
		Last Modified: Thu, 02 Oct 2025 02:47:25 GMT  
		Size: 69.7 MB (69687587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c1d564aa7790005af29916aaa660a495b52fd14381db84a19e46acc186baad`  
		Last Modified: Thu, 02 Oct 2025 02:47:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc932371bd18fee54f4984579ca02fb48890d20d460a1fd42b259c8d691fc872`  
		Last Modified: Thu, 02 Oct 2025 02:47:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3ac0fde0714e9f2e80e4176bb4d5ba39d23a591231e20f562aa198dea2dcd640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3270c962249eeb573c41d5c357e6e12377810b62f490d6911c61c34027be515a`

```dockerfile
```

-	Layers:
	-	`sha256:9fcada49c0a239ff9aa85db28c0df8e997e28a03f91386b4d9c053a6f66fd911`  
		Last Modified: Thu, 02 Oct 2025 06:46:11 GMT  
		Size: 7.4 MB (7352113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89898f1107523fb809a2710773cc83db0490b9b29a7fd4407f458911f517578e`  
		Last Modified: Thu, 02 Oct 2025 06:46:12 GMT  
		Size: 16.6 KB (16631 bytes)  
		MIME: application/vnd.in-toto+json
