## `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:e8d3680a36e58f602a9b659b926331fb123b9aa3dab539ff0fb9ab783755b2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:93ceebc32f4b32a15a6b96daa3ae8f23ef53d79fd5838d75f665dd0898253518
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269348015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c8708ecdf8645e10f09fdca222b13d217d3d7da20ff180711abd16f0e9c30b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:11:09 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:11:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:16:27 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:16:27 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:16:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:16:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:16:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d7fef2171261d35cbe76cea836569a7106d2a9523d9a32c74193df8b83e18`  
		Last Modified: Fri, 02 Feb 2024 17:31:44 GMT  
		Size: 145.3 MB (145271036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5e9fda68b6c0bf08b612d1ddd876138e589a6b19264ab966e05f4cb96914ff`  
		Last Modified: Fri, 02 Feb 2024 17:34:37 GMT  
		Size: 69.0 MB (69019398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b472cf07ae84b9f4d8d4f677caf2f7862f06eecceca2dcd5da9ebed1e30ab36`  
		Last Modified: Fri, 02 Feb 2024 17:34:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6caac1b5f8205f4b829e5e0e9481c079ef7730d0734e2ff1fc992d57949bd11f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264867564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d897ed1972ea80e6a75cb7880fc1451b472ea59b61eb442418c49747d291e3df`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:20:51 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:25:43 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:25:43 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:26:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:26:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:26:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b439db64bcde69fb388115b6850434c56a98c6d0d363997cfa20eb0a1fb35d9`  
		Last Modified: Fri, 02 Feb 2024 08:38:45 GMT  
		Size: 142.0 MB (142006376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d416dac33fe941119dc8de46ad9401615a50221cc513a5c25722906ed77ab2`  
		Last Modified: Fri, 02 Feb 2024 08:41:19 GMT  
		Size: 69.2 MB (69152302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25661493ac05ae748c38ba9836d40228077884578bea4db99111d12a9a51615e`  
		Last Modified: Fri, 02 Feb 2024 08:41:13 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
