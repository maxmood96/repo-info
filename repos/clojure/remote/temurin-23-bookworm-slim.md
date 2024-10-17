## `clojure:temurin-23-bookworm-slim`

```console
$ docker pull clojure@sha256:5399ff2e3c7ffe1608b5392af356df4282e24e950f83f15acb025fe1aaaa9561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm-slim` - linux; amd64

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

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-23-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5725a9732abd0aad67b9109b7b1292f453e9b6d7bfd20a98bce39ceb2a9727f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261755577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb918d864dfa89d950bdbea3e86d360765af7f110b7d2dd02f741f54a2a56fd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851cc9fb21ca2ac3e3b1cefe22c283c974831b271df8829329a5ef738df50261`  
		Last Modified: Sat, 12 Oct 2024 01:33:12 GMT  
		Size: 163.3 MB (163252850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776dc9f90a57090783636b142c511ededfcd0e6370864f2165cef8145496049e`  
		Last Modified: Sat, 12 Oct 2024 01:37:48 GMT  
		Size: 69.3 MB (69345317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c53cb91a1e82c44bd65aa003137fd75b357c1742beb7bddc1ff716fef715e`  
		Last Modified: Sat, 12 Oct 2024 01:37:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea752e380c96041f3a6dbc234d8c93ff2cd97acb5bfb496910c1e933410364e4`  
		Last Modified: Sat, 12 Oct 2024 01:37:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65063e368b07fc979c03b059040fc05df6b8a42ecbffa5bd9d913310bbd2a162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dbf2249e714d51b02d70a417978736a182568254ad4de9c0ff395253212ce9e`

```dockerfile
```

-	Layers:
	-	`sha256:db0a4fc784ac1c540c9f074985815d31015ad42e38c24b3a7c4d77ec0f4b31a7`  
		Last Modified: Wed, 16 Oct 2024 02:42:16 GMT  
		Size: 4.9 MB (4904988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d89bc625e1cf3c7b19b587de5819f847146d39c1eaa59427f2fd025718a1f2d`  
		Last Modified: Wed, 16 Oct 2024 02:42:16 GMT  
		Size: 15.7 KB (15656 bytes)  
		MIME: application/vnd.in-toto+json
