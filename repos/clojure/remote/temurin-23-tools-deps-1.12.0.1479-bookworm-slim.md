## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:0caf84335f864ba258bd68b1f4fb53714edaa55d913e7aababb89188f3066a87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:77cb3486d18e954b545406d955f7b797e2b9332cb59a5fe443441499a88949d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263877461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b981414b3883067be23959dd927dc1af5ac69e4b061b8076051996da14b176f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb4210724a31037da3bd0c038a3cbf334515c0d34be8f9b9fa37447de3afe9`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 165.3 MB (165267658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65507b66b947e95ffd1d950355979fbc68129b0af64e2da5dda642dd85ceca58`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 69.5 MB (69482476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca001bdb18c6b7494446501fb7cafb9b842c2361f55407154620a6dc5190f43`  
		Last Modified: Thu, 17 Oct 2024 01:13:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32b47c8fcecbba49bb8ade1d292ffc4ca01e6ca204d1caf0a1789bfba2ae450`  
		Last Modified: Thu, 17 Oct 2024 01:13:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:952b92a4f64576db4238cb969332a4e7a5334b1748a435451b3537a051fa8398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9888d5022ebb9b4d573d6705aab7de09622bd3f54d4c70cda209fd72c3cc1210`

```dockerfile
```

-	Layers:
	-	`sha256:1df74389c19c19e414e4ef104eeed5756874b26ce39cbae291dde4c79e851c4b`  
		Last Modified: Thu, 17 Oct 2024 01:13:42 GMT  
		Size: 4.9 MB (4899844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a71ca23345e7e3b7eec68e2bd10bab5a1a76ca3f91fd604fe6d747df68addacf`  
		Last Modified: Thu, 17 Oct 2024 01:13:42 GMT  
		Size: 15.5 KB (15549 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70230f19584ac873ec490b165791b20961a199f7dcd750e2c09f2b063bd67022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261755300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c4eb44dba8faa4b36e2a25a8e1d385692501a9475e6e5e1db6c13442e624e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7943d41d804563f03bfbce62b1be7dded9a88ddd348486736a41f14fb75c989`  
		Last Modified: Thu, 17 Oct 2024 08:28:47 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e7dc8e4cee0156078036fa6468f138f75ab3bbfddf5b98156280e4abbc90b2`  
		Last Modified: Thu, 17 Oct 2024 08:33:24 GMT  
		Size: 69.3 MB (69345119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283773d967eae6c70a240cecf0d0b6521f922cb9c533e96ef79d9367539cfedd`  
		Last Modified: Thu, 17 Oct 2024 08:33:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3361b0a2d491ec394063f36c727d863353807703307ea2a1ea60cf09d4c2e701`  
		Last Modified: Thu, 17 Oct 2024 08:33:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:610f8a4a3cadd2b39fc1ee038ee77d3930ddae2b3abefc3dc2f5f8764c947b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2955a7a2e42230d552b3989ac416cf9302d3f8fce92b047dee1d564304a7614e`

```dockerfile
```

-	Layers:
	-	`sha256:dfbebe01b74fed0e40962f610724842d03817d58269b2198d88140fbd6814d14`  
		Last Modified: Thu, 17 Oct 2024 08:33:22 GMT  
		Size: 4.9 MB (4904988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5451f7597af63434f1083dd5d0662b37fd6c7959207e846c5b93657d7512b50`  
		Last Modified: Thu, 17 Oct 2024 08:33:21 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json
