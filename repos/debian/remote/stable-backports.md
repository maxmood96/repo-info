## `debian:stable-backports`

```console
$ docker pull debian@sha256:50b2ee843e2f1f46409741a18f017e1516942b6730c0c43219d229e806db48c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:d7e571966c110afcc4c601b7f297f8af6f0809b83fa449ff6df582cb3403237a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50383081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53feacfa691e2ed10c876e5c8f654ac73e96075e2bea256d58ff90ec87813bda`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:21 GMT
ADD file:fa5e41bdd83bdcb44dba68dcf6fea81a4556ce01f7ede8168839fdcf0aeafb74 in / 
# Thu, 23 Apr 2020 00:22:21 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:22:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ab068d65c76515479a49d963119d9c4c88be2a322583227532edcd053131d61c`  
		Last Modified: Thu, 23 Apr 2020 00:27:12 GMT  
		Size: 50.4 MB (50382859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39e0cbf289adeac97b432064df46cff67e35441e001233ca4d3339e9affa41d`  
		Last Modified: Thu, 23 Apr 2020 00:27:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fffee85ba06b4ba5b917ec6fc78cd1061e3337acbd5618e13d9d5fb0f5d41968
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48096963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c4d17ecbe175a7468fcd9a9f312c88c29644c59e04da38b835c9a2a416617e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:55:04 GMT
ADD file:82c130da53ee3bd119b10da370ede912b233caa259bfb647ca931feb92be2dc1 in / 
# Thu, 23 Apr 2020 00:55:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:55:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5252cc0bde5f71c14833a3a353f87d023c7ff6c96b5178d86b5f2283abf7252a`  
		Last Modified: Thu, 23 Apr 2020 01:02:54 GMT  
		Size: 48.1 MB (48096738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8bede32ccc866a77d3f3975c0b52cc8183a622b26d30e5bcf519e04da531b9`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6326e8387e3c67ca7f7c2cf9bd1f9b643dac1ebc5ab08f014fb34f1c0f83156d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45864476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05801ca39663264ca7697755dd914831074f3d340474fcb4f5bd89831350d90`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:06:28 GMT
ADD file:53fa4fe14c5497c53f369d4ae850143c2f49ab2b0c387c25a46c54846ce1168d in / 
# Thu, 23 Apr 2020 01:06:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7f3350e38ae27ccdeab9f12ddc380f1cd85f75e91209e3c7d806589ed4dcc312`  
		Last Modified: Thu, 23 Apr 2020 01:13:39 GMT  
		Size: 45.9 MB (45864251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3196bfebdb60d6a7d2e6563f2a7019549aef196de55a5e91fd31c52c75dc65`  
		Last Modified: Thu, 23 Apr 2020 01:13:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f8455cbbe78959a2f274b47cc02b999acb52f3030924397a9f151343170cfe86
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49169932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6a15b154519ee00800be56e8c26b8c792854ed4ab3d836ca41dee467b7aef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:57:23 GMT
ADD file:f58df661184a316f34dfd64bb567557a1f83c7bbd17792a4ad81d1105bc4e6c9 in / 
# Thu, 23 Apr 2020 00:57:29 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:57:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7c0261aebf5569da4bc33f272658f5fa8486f16c4dd986c8792ba3b5a8ad0a5d`  
		Last Modified: Thu, 23 Apr 2020 01:04:53 GMT  
		Size: 49.2 MB (49169706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7315fb2066cfb9925d0295f354f3452d26533ea8cbbc95bad6b3a9fe1dc30889`  
		Last Modified: Thu, 23 Apr 2020 01:05:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:3f55e03dc399277c9a9d44571b84de8b0f588645c6b1320d172508a92dfc1102
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51147195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0495de66f843e4ef53fdff97a3f522abc087b7e4fc5e308583c83a34ea75b566`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:31 GMT
ADD file:da50ddd228ee07b54262e4379379f3f7e8ada106fc660fbc09fb47145590f85d in / 
# Thu, 23 Apr 2020 00:41:31 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:41:36 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4088cfbfca15fd87713a59e1368a9cdda9845981615080cf89f5c7b1accd331`  
		Last Modified: Thu, 23 Apr 2020 00:46:44 GMT  
		Size: 51.1 MB (51146972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00092cde2b0217ddbeb87b0330a471c4ffc9c54d02f747b66ce91696fc58e9b7`  
		Last Modified: Thu, 23 Apr 2020 00:46:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:639b176e27fb227c06ed1318e504daadeb4281f73d8219b1a515701e0001ac30
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49019385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df606ffcb68f591ac21c81e6aecae0920cd3f3575c35d913341080b4449023b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:11:42 GMT
ADD file:5a0065ff326073bf141f8523672b836937bbf34a234e73e42466ed4e18e3bdd7 in / 
# Thu, 23 Apr 2020 00:11:43 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:11:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:192cb836eb60701de82e3544a2c2279127dbd4f93030d06a700b28355cee7d0f`  
		Last Modified: Thu, 23 Apr 2020 00:21:17 GMT  
		Size: 49.0 MB (49019161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f26bb7e4228c121e48d3e89dd9fa8569c51bffc6ce0a89cd6c5afed485d2d3`  
		Last Modified: Thu, 23 Apr 2020 00:21:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f0101b3ffaa629cbba3edc80e46f4c3a71835501a7ecff4e981fc807344fc767
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54139822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb52e62651bf5ebba1ac6a9ed79d03f0e3b87749df423d83a1d997bba037b2a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:40:13 GMT
ADD file:352901ca72bb329990bed05b43df906f3e61a21a39acf4e7c9a4426339ace2f9 in / 
# Thu, 23 Apr 2020 00:40:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c9efe11753157bb4a8b8a89e3186c0413b69200a36afd569d90ccc842a051bf7`  
		Last Modified: Thu, 23 Apr 2020 00:53:23 GMT  
		Size: 54.1 MB (54139597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd08b9c0abc67885550a2fbb8e7241b0fd376f9a1f3fcf8f2c5b861af6c815f`  
		Last Modified: Thu, 23 Apr 2020 00:53:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:ccd6c465dfab13dc34435ca29fd2c76a5d058bf78dfdb1dfb0dd4632150fd436
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48960377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e4cacca78fad6838102a11df0e44ae68e8dd8591e17788bdfc08dc4274ca2b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:52:57 GMT
ADD file:dc742545e62c5897397eacfc112a002a7cb3c762b714b9d0912e6543625c9209 in / 
# Thu, 23 Apr 2020 00:53:00 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:53:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6038b51170e5d913c266f2fcd58d2470ed62a428366703e9b459f962816767c5`  
		Last Modified: Thu, 23 Apr 2020 00:56:58 GMT  
		Size: 49.0 MB (48960154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4679175353eab49a667ab30873ca53b9cdca4cd6ce9076eca4093b85b30d6d73`  
		Last Modified: Thu, 23 Apr 2020 00:57:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
