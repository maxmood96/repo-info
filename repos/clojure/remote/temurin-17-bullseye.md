## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:5ed6b9c7a620e4294a198d4e3e1f2a9447754dd835bf6f57ba858797e22c0b29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d9c73b9aa1a8bf461913e6b4d00453f947af20aa5bb3f5fbbd05435c0882ea91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268011964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09303bdb6c6ce381c2bffaacb690fcd4c79434186c37c60b5ee88490d7a4d1aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:10 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e494affda65090320d7a49c99e2e8660f342cc6e625d0528317b222a11896b8f`  
		Last Modified: Tue, 04 Nov 2025 00:55:45 GMT  
		Size: 144.7 MB (144693282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fe96bf7d1bec75a0f6c00df9fbc4ec6e4cd3ac5c9aec0d5f0e36040cc7110d`  
		Last Modified: Tue, 04 Nov 2025 00:55:56 GMT  
		Size: 69.6 MB (69560953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cdd86f88c9ec997572a907533bba9a73c3fad6eb42461ac3883968a45f0802`  
		Last Modified: Tue, 04 Nov 2025 00:55:49 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36380ff8ac5f587bc5f98d8698133fb82ae7e767c1573395afb60bb34533b9c3`  
		Last Modified: Tue, 04 Nov 2025 00:55:49 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:888bd4689f9a08582ddea42fa3b35427ecff6f52e2e6874e1400e12d6605ed7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecea6adc7e2d5fda624baa404a0dfb7af7326cea8722425767f5d10b4e4b13e`

```dockerfile
```

-	Layers:
	-	`sha256:44c523c19961f8512202338aeb2ee4a19e7acd569a43d034544c8dafb96dc24e`  
		Last Modified: Tue, 04 Nov 2025 10:39:18 GMT  
		Size: 7.4 MB (7395667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c0c9e047ebdbdef7ec03b39df6872f4bc4afc7c620e5cb170ddd43cbc01596`  
		Last Modified: Tue, 04 Nov 2025 10:39:19 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:18dedc34e4066d04c123b49985d69d220f344bfc95ca84c7500906b290d5c3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265489301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294b223ca2e8027e220e574d769d77ac7fc893a94469e5a2864405aadb383c4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:48 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d692e9a227ecfd32c083e859b1d153bf7e0fc33a28532e567002640ca59695`  
		Last Modified: Tue, 04 Nov 2025 00:56:27 GMT  
		Size: 143.5 MB (143542161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804abf5e26df8103906b624a3867f5e18038ee6b88cd49b92d973515ee511cfa`  
		Last Modified: Tue, 04 Nov 2025 00:56:37 GMT  
		Size: 69.7 MB (69688133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e0e1a260d5922d769b0ba1273a8d3a4fb74360007a300abcdd36ff2e4c6fc7`  
		Last Modified: Tue, 04 Nov 2025 00:56:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d4f8af7df8a65c9671c79dde9450093e76ae50b8e8c57dd3735682eb99a2e1`  
		Last Modified: Tue, 04 Nov 2025 00:56:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:afe941b95ea9619855fd5b090e0e3e94d9ad24872df49888c5e4d6e087f68316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65995b695f1033c91bbd80851a62c637f2db9f6468e73aaad4fddf4620ef61e`

```dockerfile
```

-	Layers:
	-	`sha256:a218e2a05d3edab25f0112108d0b547dea7bdf31b016be4e026fd54acbeb8292`  
		Last Modified: Tue, 04 Nov 2025 10:39:26 GMT  
		Size: 7.4 MB (7400766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f4da5d79dcb4cb8b7d13ea0f8543971412edf3df03976dc49b5d26bb7cfe3f`  
		Last Modified: Tue, 04 Nov 2025 10:41:10 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
