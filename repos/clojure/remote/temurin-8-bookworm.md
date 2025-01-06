## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:df5404d5682c60fb7ba00eb015bf645386200e6b77ae146bd6ba7e7ad0d9d9e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6494cb06446e1556952b92a95886c2cf076e4f4c9161c8502c0a88c3c875ec26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232875853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe612dd38b3ecada246d8957cbe3ae2f7fa2921c30ff7f64e11c6b52e9f0986`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5728d0cc91270c67f82bfbc5eb18d02f37da7403c8da347604aeef04b1b9a2`  
		Last Modified: Tue, 24 Dec 2024 22:37:09 GMT  
		Size: 103.6 MB (103633884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec0e501bf70fc5ea84829b6f34ca3250379f8a58665f4d9e4ea370a4bc093b`  
		Last Modified: Tue, 24 Dec 2024 22:37:08 GMT  
		Size: 80.7 MB (80744260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326091088a83804c87648f87581ff95d7b9ae377074199becbb22cea9bcfb9b`  
		Last Modified: Tue, 24 Dec 2024 22:37:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:636711818699852f4af46ad75e337531ed4c5e7da67eb2e721d4d1073c9ba165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e40c33525606d6c7c3775e6ba35f4ae30444fab735530eb3a03f66903d563e`

```dockerfile
```

-	Layers:
	-	`sha256:6d29117178a782b42058f2bb2da76af92811947cd2be7c43e83e3aa0939e5805`  
		Last Modified: Tue, 24 Dec 2024 22:37:06 GMT  
		Size: 7.3 MB (7293236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12f526139d82fdd73d6af1f9d6e5a2729ca4904c62e538056df4021e29155e3a`  
		Last Modified: Tue, 24 Dec 2024 22:37:06 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2226fa131eeaef4248bd3afdef33efe545684f37e3e94ec7261998e7a51e9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231678786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1a0b3a556705f711d1b5fe5d373bf3a19ae5b0e87610f31c8b5e9983098ffe`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112fd3c245deeaab14c956138bcb866289ea45497d0687528ac34f2dd5bd159b`  
		Last Modified: Wed, 25 Dec 2024 07:11:16 GMT  
		Size: 102.7 MB (102747746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a735c209ce3bebe25c0015832506038e64eb70bfc50a6887a66383ebee5f2d`  
		Last Modified: Wed, 25 Dec 2024 07:14:51 GMT  
		Size: 80.6 MB (80604911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c5e7ed41ed1a3c9bfdae50784ffb22816f48d96b31dcec28d00ff3f4b680d`  
		Last Modified: Wed, 25 Dec 2024 07:14:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:38dfaa911b61d28a9ded660064baa36e2ccb086d631b07211cf30ca493d79b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f704dbe9fce3e177c80db24daaf968ed903ff7793552d871fc5c3c76a001285a`

```dockerfile
```

-	Layers:
	-	`sha256:a2842941ddf1269c8ea085a66a4e764c9580e07274b214fb3ac1940c08bd8adc`  
		Last Modified: Wed, 25 Dec 2024 07:14:49 GMT  
		Size: 7.3 MB (7299697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa21da9c4b7620ba45eacace4cf8c6aed0b07640158703799f6acb68efaf43`  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
