## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:df186af6f1fd5956f82c9d9575617ad1fd6d698660448ed4dcf187ac495c24aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1b04ce454d7fd7078ae673f0281116140b7bbbefb626fe31b01c6088d952f81d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193660630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62aae9d382f773d2c6e0ca00fe93a4b84f6142b7626ccce76fde77982aa69329`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:15:01 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:15:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:17:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:17:36 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:17:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:17:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:17:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eec355dced25396607810d8a074f4df2b1edf41d31600fd54b82c499259aded`  
		Last Modified: Wed, 24 Apr 2024 21:40:54 GMT  
		Size: 103.6 MB (103600133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10100abaff1378eead77419b81975f9004df8263a7ba12fe35a3aea17e64967`  
		Last Modified: Wed, 24 Apr 2024 21:42:39 GMT  
		Size: 58.6 MB (58625619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c9fc6237ee7216d6fa119ef206b94c54ac41288e2db8b13b457cedf22e8f0`  
		Last Modified: Wed, 24 Apr 2024 21:42:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7edf8fa9b7ee0fbb2d0fc9a8f3894c7db911e62150151a1f261897ddcf867a86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191540241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9156fbfc9cb6f00d5dabbb1df1b1252d913549c7ee8e0c564fe35911b4639aa5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:00:52 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:02:57 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:02:57 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:03:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:03:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:03:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1d3aa9544a8fa97e0e443515a329cf4c529fc91820fd3aa9ee9f1b352ffa51`  
		Last Modified: Wed, 24 Apr 2024 19:22:09 GMT  
		Size: 102.7 MB (102700111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9965605f784a15aa1e60f5bed82f6491ebd6791404d0b35f5bb3b2ce113a8b9`  
		Last Modified: Wed, 24 Apr 2024 19:23:45 GMT  
		Size: 58.8 MB (58752179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f652ab5304ecbefa5733ef9386fe99c0e08fe0cd77eb9287a45d64186eb57bc6`  
		Last Modified: Wed, 24 Apr 2024 19:23:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
