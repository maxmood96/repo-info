## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:5ece9e5f714b78b66625b1b136ef421d02006316754e09092df7017b1ad30731
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d702735a71919aebfdebcb4cc8751d366663ee0e4e9ded4d3aacf3b89d461500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227706634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9976ed6ae0faea2a33b40a4ecd8f8fe3d9da0d576c91b6e89657a45b7106ecf9`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1febeedaaa2c1679a06b68eb80c884ba1fd80a38fec0b7c8bcc896119b6977b6`  
		Last Modified: Tue, 23 Jul 2024 07:13:44 GMT  
		Size: 103.6 MB (103600204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa08015898b2285169fb1eb11c27319e016d39e3f6d5b4ad416cd2a4da9da30`  
		Last Modified: Tue, 23 Jul 2024 07:13:47 GMT  
		Size: 69.0 MB (69021208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc09eb215c8608b87b396b4855fe043939b9227aa1e5c23c210c14021feab1`  
		Last Modified: Tue, 23 Jul 2024 07:13:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f22502a1d7587e37bbb1b8e9f4e8ad74ab6a6161c3c07a44b9bb4b35f546d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57eff1b6ff01d04cccb3d626a66d3e9953a2b7175482e09a446636bd3dd222`

```dockerfile
```

-	Layers:
	-	`sha256:9fb72d91bb76722ce100450c819c91932c5cb0458f95b0e7bdd964a112ee8ec9`  
		Last Modified: Tue, 23 Jul 2024 07:13:47 GMT  
		Size: 7.1 MB (7065835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:932c9b928f5122f3617350b01f0b52310ce1f11d3646a4871fec7a57beac1435`  
		Last Modified: Tue, 23 Jul 2024 07:13:47 GMT  
		Size: 13.8 KB (13850 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b240a8527b4b7cd2f9370a045d04d935156739ea81c0717bd7a2734708917a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225556764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4361e6e5228f99b3ec106858fc8b9c54e00b772cadb5373278de63f1eb3e6f2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15853bf8cc7cb890eaf09b1c679e02958728ad26cee6a9f618aca04b89974d99`  
		Last Modified: Tue, 02 Jul 2024 09:12:42 GMT  
		Size: 102.7 MB (102700427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded1aedbb29f746f14517c1a96e649cf16564c09ed3e40beace7a196aade626b`  
		Last Modified: Tue, 02 Jul 2024 09:16:40 GMT  
		Size: 69.1 MB (69134038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5b4db452ea8db81fa8e1ee8518363b9e11793bd190c21e105d6010ef0db1bf`  
		Last Modified: Tue, 02 Jul 2024 09:16:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:35ee4209e1ccd6e8d84f61d932b93aa78bb1860b165dc2430b67ac6f733b08a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7bda2853d87b4652bb0d0102c875c3c2105c7821ecd38c1087d9386baccef3`

```dockerfile
```

-	Layers:
	-	`sha256:8e89fbc92820486615bd99c87a33b9bd657f6acfb42e137a0af8224c7e14d46d`  
		Last Modified: Tue, 02 Jul 2024 09:16:39 GMT  
		Size: 7.0 MB (7028000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c23739374f3883faf20306e5788992354d2014f1c0f04a7bff80df554e3ed9`  
		Last Modified: Tue, 02 Jul 2024 09:16:38 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
