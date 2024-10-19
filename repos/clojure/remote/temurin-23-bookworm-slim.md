## `clojure:temurin-23-bookworm-slim`

```console
$ docker pull clojure@sha256:e633bd538989153fb963890399d962c0766452b3d467d7608eef41516f25e241
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:58c2e3dbd78d31d6e7129deccc10d3d9e50fce8d9383d1233fde655a4620dd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263877652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aacf0f6ef0bd127ec1130730160faf464552b5f1f04a47d2405e0aef1d165c6`
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
	-	`sha256:86c28068f9f09c88174d8acdb119b86d61b43f3f0d13636ccc16755deb111171`  
		Last Modified: Sat, 19 Oct 2024 03:00:06 GMT  
		Size: 165.3 MB (165267610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dcfbb93e6b21dde577e8ee1d0e3d1dc9a6b029e33c5b827f70fd455341b451`  
		Last Modified: Sat, 19 Oct 2024 03:00:15 GMT  
		Size: 69.5 MB (69482713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633c91e16c3ae3b6300c898ffb89749376fde45a4134dde6bc0e1c9363f1ebc`  
		Last Modified: Sat, 19 Oct 2024 03:00:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397692259f6dd8e44c80c8dd21c992e8de3bba7b3a5d093c9ae9c4b26bb1e7b6`  
		Last Modified: Sat, 19 Oct 2024 03:00:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33f6e798109979c0b9d7d392760e18eb3abf66630113129860dc22c70b9b534e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214967443ce7a966ac3bc1fc3071df6fbff61e2d5dbc9ca353e5f8357ea1c19e`

```dockerfile
```

-	Layers:
	-	`sha256:19b7a117cfecfa82e784d893011cc1cc75e3ee11438be1ed0ccd479c9bddac9a`  
		Last Modified: Sat, 19 Oct 2024 03:00:14 GMT  
		Size: 4.9 MB (4925589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed98241df7664dce2b8432cdb1c3b1626aa51cc99605c3604573a67e63cd3652`  
		Last Modified: Sat, 19 Oct 2024 03:00:14 GMT  
		Size: 15.7 KB (15718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

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
