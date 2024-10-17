## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b1b4616fa4f42e276510c4aa4810247be37d508b8ab35b0b0a90b98e2ef974c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e71a16275faadd13b17afa11458da1c761a0204a43f88dab5110b5b3b485e92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678334f08187181d58c77a3fda86c81bb91810c182d599826c0fc13548c90739`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d8ce46e06609fbeb67fa542d703751b00fe6344a35ba9dfa19098da6848e3a`  
		Last Modified: Thu, 17 Oct 2024 01:13:25 GMT  
		Size: 103.6 MB (103611899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a8dc739be18a71cd715b1b823e770f3ea801709ba2f36c8db2c44d75d0b68`  
		Last Modified: Thu, 17 Oct 2024 01:13:24 GMT  
		Size: 58.9 MB (58939951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6777e6103741036b7f71e1c15321adc21404612b6c5ff2cae783c0444a25ff`  
		Last Modified: Thu, 17 Oct 2024 01:13:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49e6c35e990d75bf27667e73905487dd283aaa4f442481e986b969372100e41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d556bfbb4c8c9319b8020d7b826f0b6dc7d4f73ac003266841ebcf2ed15fc878`

```dockerfile
```

-	Layers:
	-	`sha256:67635ae00ce98a1fbaad0a64df845dd20a861450de72abaa557662089e87bed5`  
		Last Modified: Thu, 17 Oct 2024 01:13:23 GMT  
		Size: 5.2 MB (5221741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf17fdf7e36420db492506b8cc7248e6eb955f2fe08298c86eb625b7daeeba`  
		Last Modified: Thu, 17 Oct 2024 01:13:23 GMT  
		Size: 14.0 KB (13959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50532f2ca10ef5d9dcb0bf24d94850745cec10568b1bc3ab97be89fdec0b7d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191877899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91349f1f4eeb1bf7381f11b97c110e7d9b0f74e0a834b3dffa1bab610afd0800`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb75fe23968e35e453b89cc8dd158cce9129a4418492f492ec116f1b8ed71cf0`  
		Last Modified: Sat, 12 Oct 2024 00:58:35 GMT  
		Size: 102.7 MB (102729198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d3b3c1b95f64d8468a23913509bc6d83f742ff63e7437013d66e40fed8d70`  
		Last Modified: Sat, 12 Oct 2024 01:02:57 GMT  
		Size: 59.1 MB (59072897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fec10c386b5f4dd0b4a042c5a353d324b11008b6c2703c35abb55709b8dac5`  
		Last Modified: Sat, 12 Oct 2024 01:02:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13f3de5310639170d5e654e74cc502a3547b5654172f87057af7cfee12d4acf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356caa7a6600ae791fed3ca9cdb1a65d545beb93c036a98ed38d2a7ebc3e20bb`

```dockerfile
```

-	Layers:
	-	`sha256:a0bfb3a8fc689cf334286f2ee134ccf4513a9cd875f770da164aff68bac2ea8c`  
		Last Modified: Wed, 16 Oct 2024 02:09:15 GMT  
		Size: 5.2 MB (5228087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055d42b502912f7326387072090909f2e3aea59f635502f158e8cc7ceabc3cdc`  
		Last Modified: Wed, 16 Oct 2024 02:09:15 GMT  
		Size: 14.1 KB (14064 bytes)  
		MIME: application/vnd.in-toto+json
