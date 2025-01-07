## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:435dfb6507d77aa913503548f7879b73778e11e81bb530f8f70d2c4ebf1f5762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:90c3658f4f786e7188b0196164346806f219d890733f0ca00e1cb697a801222d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232907717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f28e0feb1633e1f2f9462d03ff18c765933093d2705b1ef0149711e3c8460c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6930a8bf16748ee896e7160d547055aa58ca8ae63753ba641fffc34b8007ebad`  
		Last Modified: Tue, 07 Jan 2025 02:29:29 GMT  
		Size: 103.6 MB (103633892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a636c92ef932a7ce4b564e45983cfbb42243a700a18fad9f12e1f537a21772`  
		Last Modified: Tue, 07 Jan 2025 02:29:30 GMT  
		Size: 80.8 MB (80776117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230822e5faa9e6e89295b86fb3006460531af5c3cba38654927e51698d986a4`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f5562b2e624f1aa4a2f9fb961acbcabd3145c7a15fd07215c4c56a8ec932de01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e6b8cbcfc0a1acff10f0f14a502c9d9ead2a989759945df5d4fa189db90a43`

```dockerfile
```

-	Layers:
	-	`sha256:6f4f5b17d7a52e50fff257116a485e2ee4a1b3875c7bcfbb8fd72cafdaff1578`  
		Last Modified: Tue, 07 Jan 2025 02:29:28 GMT  
		Size: 7.3 MB (7293298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5aa18d87ae7ebe1cac278e08a9045925b3cb161f4d637789698cc20f1171927`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

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
		Last Modified: Wed, 25 Dec 2024 07:14:49 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
