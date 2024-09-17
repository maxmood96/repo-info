## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2c3528bb8c029cb7395572eef8991798cfec5cab7eedb4870d9b0fe8d5bb77a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:46670ce6ac322cc9b92233d4f102509c7756a64f6dce0b1f56bed845a2aa47ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244159962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d10f2743d6231d3537e08ceb4ce5a6e97143838e1a3bdda71a0909de731df7a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5940729d553ccfbb3f18a7e97b8c7a7908c1075be50b9f6a44fca0b8522cfc71`  
		Last Modified: Tue, 17 Sep 2024 01:56:51 GMT  
		Size: 145.6 MB (145550026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eb27f817d05abebd9f5c9d6b4fb1c057f891a2a637e3cbc63a6c8445c7c089`  
		Last Modified: Tue, 17 Sep 2024 01:56:50 GMT  
		Size: 69.5 MB (69482806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0fc3ef0955baa849602bcea9f2cfd4b927236220f4f2c38ea170ca6294603`  
		Last Modified: Tue, 17 Sep 2024 01:56:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33005eb7c29b772c1b049f87d6f805ef2d5d1d4b147229533f10cce9c2989f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be77ebfe7bd9ff1836ec5d4f52d95b1e9b5e0e50f527585421dd3f02f2638ef`

```dockerfile
```

-	Layers:
	-	`sha256:b157bfde0bc79180c7398cdbe6d774685b413a9ddb7158d30e9772a1f5e13df1`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 2.1 KB (2119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d930a32d08a8adac97c57d099e4782f9f3af9dfd54dd1108140bee3fba2318f6`  
		Last Modified: Tue, 17 Sep 2024 01:56:47 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:083b1088fa73a4ce2fc05c3be01e69dc2167953813bd6cda7331278f10dfa4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240856487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbba409660391f7a73a2db42752c9c4464a44e19086520b3c05b5439760b8b1`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d47b458c8c18ce1896657ea931977961501bbeab7113170bac391a26a27601d`  
		Last Modified: Tue, 17 Sep 2024 04:19:29 GMT  
		Size: 142.4 MB (142354737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ca71316865c0263595f246a34ba89ae1455690e4db4f8c395cc2b7fe749b5`  
		Last Modified: Tue, 17 Sep 2024 04:25:56 GMT  
		Size: 69.3 MB (69344558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e845307c82ae4464505e613a290432e766664b8f9d438432226b8ec95b1eb16`  
		Last Modified: Tue, 17 Sep 2024 04:25:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb60611510ac9878be4cdfe69fde221829ce6c0036a9c75f15411589cf4c6a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48844d5feb3aab4927a01701c580c338d23458e80f05070ead23783c5bf548e8`

```dockerfile
```

-	Layers:
	-	`sha256:0174b5923c88c045eb2475ddc8310a925e86ebf3dcc372c1b6851554e1df2866`  
		Last Modified: Tue, 17 Sep 2024 04:25:54 GMT  
		Size: 4.8 MB (4751577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d5deae37847c5b6d9b4e1dcbad079dff90dd163078adc2b71d69362e34ddea`  
		Last Modified: Tue, 17 Sep 2024 04:25:54 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
