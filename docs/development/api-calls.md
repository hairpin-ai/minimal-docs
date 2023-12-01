*API Calls
=========

* * *

##### [](#basic-example)Basic Example

    import useSWR from 'swr';
    import { fetcher } from 'src/utils/axios';
     
    function ProductList() {
      const { data, error, isLoading } = useSWR('/api/product/list', fetcher);
     
      if (error) return <div>failed to load</div>;
     
      if (isLoading) return <div>loading...</div>;
     
      return (
        <>
          {data.products.map((product) => (
            <div key={product.id}>{product.name}</div>
          ))}
        </>
      );
    }

* * *

##### [](#set-baseurl)Set BaseURL

    REACT_APP_HOST_API=https://www.your-domain.com

.env

  

    const axiosInstance = axios.create({ baseURL: process.env.REACT_APP_HOST_API });

src/utils/axios.js

  

    import useSWR from 'swr';
    import axios, { fetcher } from 'src/utils/axios';
     
    const fetcher = (url) => axios.get(url).then((res) => res.data);
     
    function ProductList() {
      // const { data, error, isLoading } = useSWR(`https://www.your-domain.com/api/product/list`, fetcher);
      const { data, error, isLoading } = useSWR(`/api/product/list`, fetcher);
     
      if (error) return <div>failed to load</div>;
     
      if (isLoading) return <div>loading...</div>;
     
      return (
        <>
          {data.products.map((product) => (
            <div key={product.id}>{product.name}</div>
          ))}
        </>
      );
    }

* * *

##### [](#without-baseurl)Without BaseURL

    import useSWR from 'swr';
    import axios from 'axios';
     
    const fetcher = (url) => axios.get(url).then((res) => res.data);
     
    function ProductList() {
      const { data, error, isLoading } = useSWR(
        `https://www.your-domain.com/api/product/list`,
        fetcher
      );
     
      if (error) return <div>failed to load</div>;
     
      if (isLoading) return <div>loading...</div>;
     
      return (
        <>
          {data.products.map((product) => (
            <div key={product.id}>{product.name}</div>
          ))}
        </>
      );
    }