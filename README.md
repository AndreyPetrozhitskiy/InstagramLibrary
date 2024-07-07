# Библиотека для скачивания контента из Инстаграм

## Использование

```javascript
import { instagramGetUrl } from "instagram-url-direct";

const download = async (link) => {
    try {
        const result = await instagramGetUrl(link);
        if (result.results_number === 1) {
            return result;
        } else {
            return null;
        }
    } catch (error) {
        console.error(error);
        return null;
    }
};

export const downloadInstagram = async (link) => {
    const result = await download(link);
    console.log(result);
    return result;
};
