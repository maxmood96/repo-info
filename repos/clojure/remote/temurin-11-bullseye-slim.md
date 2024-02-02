## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:ea1cfa969983c802599b48079f0b08d25b5e56f3281b7c9f27cc7eeaeae666de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d3feb21a15d6fd91c7914e9afe1afa745e1f8a9a8405d17b1bb95b103ce58450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235319081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5825f172a2e6339a6ae1d3a82ef1feaf3341a406cc473b2c251604ef6142d44d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:11:43 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:11:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:16:56 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:16:56 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:17:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:17:13 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:17:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51c4479436104d74ffa4a3d93686573e899aa1d342f5c43e963b26942d6975`  
		Last Modified: Fri, 02 Feb 2024 17:32:04 GMT  
		Size: 145.3 MB (145271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa857fac542f05b36e8b38edd7cede494e4f2babc6b9b831fb4fc227049271d`  
		Last Modified: Fri, 02 Feb 2024 17:34:55 GMT  
		Size: 58.6 MB (58629618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2614b1d5384c4c87b8953b4c3c15a86f04b97a53b5ac670346b4f195a14681`  
		Last Modified: Fri, 02 Feb 2024 17:34:47 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:11cea2298015aa1fd91bc486e21d6cb2fefea45443424bd68d9a8bc387138666
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230827398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480735e57035daff23a989e383cd26f8e7f017d0426d0a831ee77dc3e6cd46e3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:21:24 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:21:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:26:07 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:26:07 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:26:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:26:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:26:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971292bc5a4cf5c576af3b6872d17499b5584c7af4217c5cd7375f2d989371b1`  
		Last Modified: Fri, 02 Feb 2024 08:39:02 GMT  
		Size: 142.0 MB (142006417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a63b32d517e31bd022cbc086feafc61f6a5dd9f11f3b4c658828ae4beb29ca0`  
		Last Modified: Fri, 02 Feb 2024 08:41:36 GMT  
		Size: 58.8 MB (58756028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5050332f7b3615c140a8107f0ee9ec9701d31930743add6a00fccdf19547f8`  
		Last Modified: Fri, 02 Feb 2024 08:41:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
