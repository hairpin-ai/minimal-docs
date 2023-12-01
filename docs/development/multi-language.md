*Multi Language
==============

* * *

##### [](#setup--remove)Setup / Remove

Search with keyword `src/locales` then setup the relevant components.

* * *

##### [](#add-new-content)Add new content

    {
      "heading": "Lorem Ipsum is simply dummy text of the printing and typesetting industry",
      "nested": {
        "nested1": "nested En"
      }
    }

src/locales/en.json

  

    {
      "heading": "Le Lorem Ipsum est simplement du faux texte employé dans la composition et la mise en page avant impression",
      "nested": {
        "nested1": "nested Fr"
      }
    }

src/locales/fr.json

* * *

##### [](#usage)Usage

    import { useLocales, useTranslate } from 'src/locales';
     
    function MultiLanguage() {
      const { t, onChangeLang } = useTranslate();
     
      const { allLang, currentLang } = useLocales();
     
      return (
        <>
          <RadioGroup row value={currentLang.value} onChange={(event) => onChangeLang(event.target.value)}>
            {allLang.map((lang) => (
              <FormControlLabel key={lang.label} value={lang.value} label={lang.label} control={<Radio />} />
            ))}
          </RadioGroup>
     
          <Typography variant="h2">{t('heading')}</Typography>
          <Typography variant="body2">{t('nested.nested1')}</Typography>
        </>
      );
    }

* * *

###### [](#reference)Reference:

*   [https://minimals.cc/components/extra/multi-language](https://minimals.cc/components/extra/multi-language)
*   [https://react.i18next.com/](https://react.i18next.com/)
*   [https://mui.com/material-ui/guides/localization/#main-content](https://mui.com/material-ui/guides/localization/#main-content)
