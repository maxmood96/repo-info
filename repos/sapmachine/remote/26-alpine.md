## `sapmachine:26-alpine`

```console
$ docker pull sapmachine@sha256:b297a2d866267e01705d9e02dd5c62392db1cccd656a77b7b95013bb8ecfb25f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:de8e82cc6b2f68d7766627dbced8343bc2dcebabc92b0fb538c5d69358e8bf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (232045832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc4b1f8b27ee11697bd30b6f6d6e3c7ab757e6f2ba3caaf69c79d0ace349455`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:57:30 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26-r0 # buildkit
# Wed, 15 Apr 2026 20:57:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Wed, 15 Apr 2026 20:57:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2446f13c1ecf21a6224ae74279e50b100c00b73a49e1ad5e1a755677f2f5886e`  
		Last Modified: Wed, 15 Apr 2026 20:57:53 GMT  
		Size: 228.2 MB (228181643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ff0ba85dc4420b6774e5d46086e363e17d7a66a7d0ba1986bdd8556cad4822e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.4 KB (509386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9a66d74815fcf1250bb3d3c17234853f1d9d27dd6ad448feb4f7cc461c52d9`

```dockerfile
```

-	Layers:
	-	`sha256:8b7c17e0726da6a71d0d33d935dc05d39aa789540cff4799f8ab44be145ad310`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 500.6 KB (500556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37ba7c299e46a5937cfee2e91d61f0a85f71ebe6177f27619c27d9c6e7ee582`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 8.8 KB (8830 bytes)  
		MIME: application/vnd.in-toto+json
