## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:fe92eef8e3e811660c882b0ed81fe4cb244153a9531a582a7685b5f481e64b11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:46c4697e38ded1b738dcddbc2379f2efd079644c63e697eb13d06744e9955f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233886271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619b241706709ed99896227245a91f906d3450a3ab1e28836f48aec9c945ba6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc491123b60af042c840929510e9b719886501f9eafc76f1f734b4565ccc3e1`  
		Last Modified: Wed, 23 Apr 2025 17:20:15 GMT  
		Size: 144.6 MB (144635045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1f5a713ac0b0743c39705c0028b3fe0c82ce7cc1dedc73776575218f41505e`  
		Last Modified: Wed, 23 Apr 2025 17:20:14 GMT  
		Size: 59.0 MB (58992761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990b72c8652f16e2ddef58926e31fd98172c142dc644a448e0718b44effda3e`  
		Last Modified: Wed, 23 Apr 2025 17:20:13 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890ed9b9ebef79a93feb565a2b8ba49c4ae8cd75713b4e32e5ca6ab98150a22`  
		Last Modified: Wed, 23 Apr 2025 17:20:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8ba5a0dc2eefff0ca4ce3e6af1893824b6a20470d9a18dccdf8341aefe911e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6fbd47f9ada87fdfed9e441bdb1a44d9bf1b69850dcfa3ba95b789a6cb5878`

```dockerfile
```

-	Layers:
	-	`sha256:6b9746422334a760a5eb004d4b175dff85ff517fde0f7ec499a5be313f514ba4`  
		Last Modified: Wed, 23 Apr 2025 17:20:13 GMT  
		Size: 5.1 MB (5119013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e307a2f24c374e3955ff9142331c3399e5d6efd3d176ee17eab2d41b0b5c0a6`  
		Last Modified: Wed, 23 Apr 2025 17:20:13 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d23041aba3d5358465a1fa8a72e7b7c832f3427942ba2c6a9c218a8acf52861e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231332123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ef38350a0467ffe827b7bbf16bd5e2cb7234f0ed74caa89ccd5e68885d3dfb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc61d01d3c1907bedb7211a2ec04da2c97e8407d17c661dbb3fccaf3036cfc`  
		Last Modified: Wed, 09 Apr 2025 15:18:21 GMT  
		Size: 143.5 MB (143454624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ba804dce129e7fc945504333792e6bee33983ecf9e5a18b664c0eb957d70b0`  
		Last Modified: Wed, 09 Apr 2025 17:36:36 GMT  
		Size: 59.1 MB (59126959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1acd4f84a90f5b3659d0db10345228dc6e36dbb00fd4e16f9836be2f24e188`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f87153d3dd33cfdf36462acc499f501dd0baf452bdabf0ccfd185f1c5e28e0`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a0a0b95e746297d2128da3630af359be8b2697b89d047009b165d8985de3051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1ff3f72b62615549d0d7c543417dfd95234f3674b94ff9fed7a633d6174392`

```dockerfile
```

-	Layers:
	-	`sha256:87ba6034729a459df29cdce31d741985ee87ad8d3a094d0c8584a971f1e10d69`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 5.1 MB (5124745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4722736cc92a92540b34e6df44c8ca6bdd18ba719eb6122764084fccfff54d3e`  
		Last Modified: Wed, 09 Apr 2025 17:36:34 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
