<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `cirros`

-	[`cirros:0`](#cirros0)
-	[`cirros:0.6`](#cirros06)
-	[`cirros:0.6.0`](#cirros060)
-	[`cirros:latest`](#cirroslatest)

## `cirros:0`

```console
$ docker pull cirros@sha256:3f35763473b8f22292e7dd36754054ccbb6f9eb86e42c71e10c2d8e095a16606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cirros:0` - linux; amd64

```console
$ docker pull cirros@sha256:483f15ac97d03dc3d4dcf79cf71ded2e099cf76c340f3fdd0b3670a40a198a22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cae1daf5f682cb6403a766b3e6afd73a102296910f27ea1ec392b54dc0c188`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:36:43 GMT
ADD file:bf4d7c23fe6b77a5c46f4c3ece606130b86aa04af3fbb2a320fb4a4d412c4603 in / 
# Mon, 08 Mar 2021 21:36:44 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:36:45 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:36:45 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:d0b405be7a3253cffc2d4b8425dd78c06d4196846dfe4d8fe45935f8d30fa351`  
		Last Modified: Mon, 08 Mar 2021 21:36:59 GMT  
		Size: 6.0 MB (5952271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd054094a03766a7be2860c487e0752bd99b1a636e189a2f9f2a29af58f2814e`  
		Last Modified: Mon, 08 Mar 2021 21:36:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a00de1ec8ac5311a5d4166e3433bb59659057b5be4de6465234975bec50742`  
		Last Modified: Mon, 08 Mar 2021 21:36:56 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:0` - linux; arm variant v5

```console
$ docker pull cirros@sha256:6004fde29f50500aa218b715c132b8d217214aebfc45d0c5e02047ad51ef8d2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6896135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070be85dd42f45c380d6db2aa9e36539ab51b113a2037fbd21d2b9315c1ffb0`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:48:17 GMT
ADD file:da9fcd1025acb12e39f02d61c9db96e5643e1b171bd7c70fc5904caca4444cbd in / 
# Wed, 28 Sep 2022 21:48:18 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:48:18 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:48:19 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:9ea391a19b65fb9cb506d6cba741637fa497f8dbe3b7aa5b8da499f89986036f`  
		Last Modified: Wed, 28 Sep 2022 21:48:38 GMT  
		Size: 6.9 MB (6894731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbf7c750324e04314e1347643bcd4429d52d0bee78d36c8ce39b689eb95fba7`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25aab29b8f4f08392ade6b9d7f6a5a6c19421b2fb9c2dbdf44898d26834a995`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:0` - linux; arm64 variant v8

```console
$ docker pull cirros@sha256:1b50a24be70579001ea2c8349e2c470be3baea691c77dd8dcd7a795295b9477f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea25b73359e2460d31e1fa7806798fbb505148a8bb10ca74fc31e457f439c48`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:40:56 GMT
ADD file:e4ad7e8f8ff0a06a00a1187410abf6f9a7b103307857239e8b23bdf786d18ed1 in / 
# Wed, 28 Sep 2022 21:40:57 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:40:58 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:40:59 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:46314231ec9fd8a50fac23daae253555d0556a7533d908a3b93a4602e68ec7bf`  
		Last Modified: Wed, 28 Sep 2022 21:41:17 GMT  
		Size: 7.5 MB (7492347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724a8a90dbc7e502f53dcc9a474cb6d8fe8581d65e3f9989069ee9400550b4d`  
		Last Modified: Wed, 28 Sep 2022 21:41:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b6992deb1b56bd12be41995e084d546fc6749515c22e71d2e49e651fb782c2`  
		Last Modified: Wed, 28 Sep 2022 21:41:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:0` - linux; ppc64le

```console
$ docker pull cirros@sha256:d73c78dc6c4a275c6cb1bf46654ede0305b76b430a8cb3e9d114315c1f4d2ad1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5770839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93df8c5c52071e4dd5e2ca046f7d33481ea590317b92611c992dc101cf9f9b2c`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:33:05 GMT
ADD file:37ce090900e2d750646c4d7da4fbb79559e30b5b817c833396c86613236ba838 in / 
# Mon, 08 Mar 2021 21:33:21 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:33:33 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:33:39 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:587c91809a2ae1af15d948969c3a1adb2aad2dbe2cbb6a2b8982a5cf9d14c7ef`  
		Last Modified: Mon, 08 Mar 2021 21:34:03 GMT  
		Size: 5.8 MB (5769433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01739d1b3e0963fe3d0194afd70a85c6098f0139dff49965d2ce40342d33de96`  
		Last Modified: Mon, 08 Mar 2021 21:34:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2169930d58d52208fd25b17049537fa4ec9192f04fc372a1cb57a20d7a8d3fd`  
		Last Modified: Mon, 08 Mar 2021 21:34:01 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cirros:0.6`

```console
$ docker pull cirros@sha256:35f1a7db39bc851b16de61e922b892d39e43768dbd511d28b8b0f352debd8359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	linux; arm64 variant v8

### `cirros:0.6` - linux; arm variant v5

```console
$ docker pull cirros@sha256:6004fde29f50500aa218b715c132b8d217214aebfc45d0c5e02047ad51ef8d2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6896135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070be85dd42f45c380d6db2aa9e36539ab51b113a2037fbd21d2b9315c1ffb0`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:48:17 GMT
ADD file:da9fcd1025acb12e39f02d61c9db96e5643e1b171bd7c70fc5904caca4444cbd in / 
# Wed, 28 Sep 2022 21:48:18 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:48:18 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:48:19 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:9ea391a19b65fb9cb506d6cba741637fa497f8dbe3b7aa5b8da499f89986036f`  
		Last Modified: Wed, 28 Sep 2022 21:48:38 GMT  
		Size: 6.9 MB (6894731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbf7c750324e04314e1347643bcd4429d52d0bee78d36c8ce39b689eb95fba7`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25aab29b8f4f08392ade6b9d7f6a5a6c19421b2fb9c2dbdf44898d26834a995`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:0.6` - linux; arm64 variant v8

```console
$ docker pull cirros@sha256:1b50a24be70579001ea2c8349e2c470be3baea691c77dd8dcd7a795295b9477f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea25b73359e2460d31e1fa7806798fbb505148a8bb10ca74fc31e457f439c48`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:40:56 GMT
ADD file:e4ad7e8f8ff0a06a00a1187410abf6f9a7b103307857239e8b23bdf786d18ed1 in / 
# Wed, 28 Sep 2022 21:40:57 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:40:58 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:40:59 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:46314231ec9fd8a50fac23daae253555d0556a7533d908a3b93a4602e68ec7bf`  
		Last Modified: Wed, 28 Sep 2022 21:41:17 GMT  
		Size: 7.5 MB (7492347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724a8a90dbc7e502f53dcc9a474cb6d8fe8581d65e3f9989069ee9400550b4d`  
		Last Modified: Wed, 28 Sep 2022 21:41:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b6992deb1b56bd12be41995e084d546fc6749515c22e71d2e49e651fb782c2`  
		Last Modified: Wed, 28 Sep 2022 21:41:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cirros:0.6.0`

```console
$ docker pull cirros@sha256:35f1a7db39bc851b16de61e922b892d39e43768dbd511d28b8b0f352debd8359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	linux; arm64 variant v8

### `cirros:0.6.0` - linux; arm variant v5

```console
$ docker pull cirros@sha256:6004fde29f50500aa218b715c132b8d217214aebfc45d0c5e02047ad51ef8d2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6896135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070be85dd42f45c380d6db2aa9e36539ab51b113a2037fbd21d2b9315c1ffb0`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:48:17 GMT
ADD file:da9fcd1025acb12e39f02d61c9db96e5643e1b171bd7c70fc5904caca4444cbd in / 
# Wed, 28 Sep 2022 21:48:18 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:48:18 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:48:19 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:9ea391a19b65fb9cb506d6cba741637fa497f8dbe3b7aa5b8da499f89986036f`  
		Last Modified: Wed, 28 Sep 2022 21:48:38 GMT  
		Size: 6.9 MB (6894731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbf7c750324e04314e1347643bcd4429d52d0bee78d36c8ce39b689eb95fba7`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25aab29b8f4f08392ade6b9d7f6a5a6c19421b2fb9c2dbdf44898d26834a995`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:0.6.0` - linux; arm64 variant v8

```console
$ docker pull cirros@sha256:1b50a24be70579001ea2c8349e2c470be3baea691c77dd8dcd7a795295b9477f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea25b73359e2460d31e1fa7806798fbb505148a8bb10ca74fc31e457f439c48`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:40:56 GMT
ADD file:e4ad7e8f8ff0a06a00a1187410abf6f9a7b103307857239e8b23bdf786d18ed1 in / 
# Wed, 28 Sep 2022 21:40:57 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:40:58 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:40:59 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:46314231ec9fd8a50fac23daae253555d0556a7533d908a3b93a4602e68ec7bf`  
		Last Modified: Wed, 28 Sep 2022 21:41:17 GMT  
		Size: 7.5 MB (7492347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724a8a90dbc7e502f53dcc9a474cb6d8fe8581d65e3f9989069ee9400550b4d`  
		Last Modified: Wed, 28 Sep 2022 21:41:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b6992deb1b56bd12be41995e084d546fc6749515c22e71d2e49e651fb782c2`  
		Last Modified: Wed, 28 Sep 2022 21:41:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `cirros:latest`

```console
$ docker pull cirros@sha256:3f35763473b8f22292e7dd36754054ccbb6f9eb86e42c71e10c2d8e095a16606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `cirros:latest` - linux; amd64

```console
$ docker pull cirros@sha256:483f15ac97d03dc3d4dcf79cf71ded2e099cf76c340f3fdd0b3670a40a198a22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cae1daf5f682cb6403a766b3e6afd73a102296910f27ea1ec392b54dc0c188`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:36:43 GMT
ADD file:bf4d7c23fe6b77a5c46f4c3ece606130b86aa04af3fbb2a320fb4a4d412c4603 in / 
# Mon, 08 Mar 2021 21:36:44 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:36:45 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:36:45 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:d0b405be7a3253cffc2d4b8425dd78c06d4196846dfe4d8fe45935f8d30fa351`  
		Last Modified: Mon, 08 Mar 2021 21:36:59 GMT  
		Size: 6.0 MB (5952271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd054094a03766a7be2860c487e0752bd99b1a636e189a2f9f2a29af58f2814e`  
		Last Modified: Mon, 08 Mar 2021 21:36:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a00de1ec8ac5311a5d4166e3433bb59659057b5be4de6465234975bec50742`  
		Last Modified: Mon, 08 Mar 2021 21:36:56 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:latest` - linux; arm variant v5

```console
$ docker pull cirros@sha256:6004fde29f50500aa218b715c132b8d217214aebfc45d0c5e02047ad51ef8d2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6896135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f070be85dd42f45c380d6db2aa9e36539ab51b113a2037fbd21d2b9315c1ffb0`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:48:17 GMT
ADD file:da9fcd1025acb12e39f02d61c9db96e5643e1b171bd7c70fc5904caca4444cbd in / 
# Wed, 28 Sep 2022 21:48:18 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:48:18 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:48:19 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:9ea391a19b65fb9cb506d6cba741637fa497f8dbe3b7aa5b8da499f89986036f`  
		Last Modified: Wed, 28 Sep 2022 21:48:38 GMT  
		Size: 6.9 MB (6894731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbf7c750324e04314e1347643bcd4429d52d0bee78d36c8ce39b689eb95fba7`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25aab29b8f4f08392ade6b9d7f6a5a6c19421b2fb9c2dbdf44898d26834a995`  
		Last Modified: Wed, 28 Sep 2022 21:48:37 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:latest` - linux; arm64 variant v8

```console
$ docker pull cirros@sha256:1b50a24be70579001ea2c8349e2c470be3baea691c77dd8dcd7a795295b9477f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea25b73359e2460d31e1fa7806798fbb505148a8bb10ca74fc31e457f439c48`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Wed, 28 Sep 2022 21:40:56 GMT
ADD file:e4ad7e8f8ff0a06a00a1187410abf6f9a7b103307857239e8b23bdf786d18ed1 in / 
# Wed, 28 Sep 2022 21:40:57 GMT
RUN rm /etc/rc3.d/S40-network
# Wed, 28 Sep 2022 21:40:58 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Wed, 28 Sep 2022 21:40:59 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:46314231ec9fd8a50fac23daae253555d0556a7533d908a3b93a4602e68ec7bf`  
		Last Modified: Wed, 28 Sep 2022 21:41:17 GMT  
		Size: 7.5 MB (7492347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724a8a90dbc7e502f53dcc9a474cb6d8fe8581d65e3f9989069ee9400550b4d`  
		Last Modified: Wed, 28 Sep 2022 21:41:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b6992deb1b56bd12be41995e084d546fc6749515c22e71d2e49e651fb782c2`  
		Last Modified: Wed, 28 Sep 2022 21:41:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:latest` - linux; ppc64le

```console
$ docker pull cirros@sha256:d73c78dc6c4a275c6cb1bf46654ede0305b76b430a8cb3e9d114315c1f4d2ad1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5770839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93df8c5c52071e4dd5e2ca046f7d33481ea590317b92611c992dc101cf9f9b2c`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:33:05 GMT
ADD file:37ce090900e2d750646c4d7da4fbb79559e30b5b817c833396c86613236ba838 in / 
# Mon, 08 Mar 2021 21:33:21 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:33:33 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:33:39 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:587c91809a2ae1af15d948969c3a1adb2aad2dbe2cbb6a2b8982a5cf9d14c7ef`  
		Last Modified: Mon, 08 Mar 2021 21:34:03 GMT  
		Size: 5.8 MB (5769433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01739d1b3e0963fe3d0194afd70a85c6098f0139dff49965d2ce40342d33de96`  
		Last Modified: Mon, 08 Mar 2021 21:34:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2169930d58d52208fd25b17049537fa4ec9192f04fc372a1cb57a20d7a8d3fd`  
		Last Modified: Mon, 08 Mar 2021 21:34:01 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
